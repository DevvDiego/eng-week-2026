<script lang="ts">
    import type p5 from 'p5';
    import { onMount, onDestroy } from 'svelte';

    let { bg = "#262626", color = "#ffff" } = $props();

    let sketchContainer: HTMLDivElement;
    let p5Instance: p5;

    onMount(async () => {
        const p5Module = await import('p5');
        const P5Class = p5Module.default;

        const sketch = (p: p5) => {
            let drone: any; // to store the loaded 3d drone 

            p.setup = async () => {
                
                p.createCanvas(710, 400, p.WEBGL).parent(sketchContainer);
                p.angleMode(p.DEGREES);

                //path loads from static folder
                drone = await p.loadModel("/drone.obj", "obj", true );
                //try catch here?
            };

            p.draw = () => {
                p.background(bg);
                
                p.ambientLight(80); // Soft light everywhere
                /* p.pointLight(255, 255, 255, 0, 0, 100); // Sharp light from the front */

                // Call every frame to adjust camera based on mouse/touch
                p.orbitControl(2, 2, 2);


                // Drone Model
                if (drone) {
                    p.push();

                    p.fill(color); 
                    //Metallic/Shiny look
                    /* p.specularMaterial(250);
                    p.shininess(20); */

                    p.translate(100, 0, 0);
                    /* p.rotateZ(200); */
                    p.model(drone);
                    p.pop();
                }
            };

            function rotateWithFrameCount() {
                /* p.rotateZ(p.frameCount); */
                /* p.rotateX(p.frameCount); */
                p.rotateY(p.frameCount);
            }
        };

        p5Instance = new P5Class(sketch);
    });

    onDestroy(() => {
        if (p5Instance) p5Instance.remove();
    });
</script>

<div bind:this={sketchContainer} class="canvas-wrapper"></div>

<style>
    .canvas-wrapper {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        overflow: hidden;
    }
</style>