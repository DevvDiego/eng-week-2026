<script lang="ts">
    import type p5 from 'p5';
    import { onMount, onDestroy } from 'svelte';

    let { bg = "#262626", class: klass = ""} = $props();

    let sketchContainer: HTMLDivElement;
    let p5Instance: p5;
    let isFirstFrameReady = $state(false);

    onMount(async () => {
        const p5Module = await import('p5');
        const P5Class = p5Module.default;

        const sketch = (p: p5) => {
            let drone: any;

            p.setup = async () => {
                try{
                    const width = sketchContainer.clientWidth;
                    const height = sketchContainer.clientHeight;
                    
                    p.createCanvas(width, height, p.WEBGL).parent(sketchContainer);
                    p.angleMode(p.DEGREES);
                    p.normalMaterial();

                    drone = await p.loadModel("/dronn.obj", "obj", true);
                }catch(err) {
                    if(err instanceof Error){
                        console.log("Ocurrio un error al cargar el modelo 3D: " + err.message)
                    }
                    
                }
            };

            //if window size changes, resize
            p.windowResized = () => {
                const width = sketchContainer.clientWidth;
                const height = sketchContainer.clientHeight;
                p.resizeCanvas(width, height);
            };

            p.draw = () => {
                p.background(bg);
                
                // 1. Ambient Light: Provides base visibility to every face regardless of angle.
                // Increase this to make sure there are no "pure black" spots.
                p.ambientLight(10); 

                // 2. Directional Lights: These act like the sun. 
                // By placing them on opposite axes, you ensure every "side" is hit.
                p.directionalLight(255, 255, 255, 1, 0, 0);  // From Right
                p.directionalLight(255, 255, 255, -1, 0, 0); // From Left
                p.directionalLight(255, 255, 255, 0, 1, 0);  // From Bottom
                p.directionalLight(255, 255, 255, 0, -1, 0); // From Top
                p.directionalLight(255, 255, 255, 0, 0, 1);  // From Front
                p.directionalLight(255, 255, 255, 0, 0, -1); // From Back

                p.orbitControl(2, 2, 2);

                if (drone) {
                    p.push();
                    p.noStroke(); // Prevents wireframe-style lines
                    p.translate(100, 0, 0);
                    p.rotate(180);
                    p.model(drone);
                    p.pop();

                    if(!isFirstFrameReady){ isFirstFrameReady = true; }
                }
            }

        };
        

        p5Instance = new P5Class(sketch);
    });

    onDestroy(() => {
        if (p5Instance) p5Instance.remove();
    });
</script>


{#if !isFirstFrameReady}
    <div class="w-full h-full absolute inset-0 z-10 flex flex-col items-center justify-center bg-[#262626]">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" class="animate-spin text-blue-700" viewBox="0 0 24 24">
            <g fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2">
                <path d="M12 3c4.97 0 9 4.03 9 9" transform="rotate(360 12 12)" />
                <path d="M12 3c4.97 0 9 4.03 9 9c0 4.97 -4.03 9 -9 9c-4.97 0 -9 -4.03 -9 -9c0 -4.97 4.03 -9 9 -9Z" opacity="0.3" />
            </g>
        </svg>
        <p class="text-xs font-mono tracking-widest text-white uppercase mt-5">
            Cargando visualizador 3D
        </p>
    </div>
{/if}

<div 
    bind:this={sketchContainer} 
    class="{klass} flex justify-center items-center w-full h-full"
></div>