<script lang="ts">
    import { resolve } from '$app/paths';
    import Sketch from '$lib/components/sketch.svelte';
    
    function changeModel(e: any){
        if (e.target.checked){
          selectedModel = "two"
          return
        }
        
        selectedModel = "one"
    }

    let bg = "#262626";
    let selectedModel: "one"|"two" = $state("one");
    let direction: null|"up"|"down"|"left"|"right" = $state(null);
    let zoom: null|"in"|"out" = $state(null);
</script>

<main class="flex flex-col-reverse md:flex-row w-full h-screen bg-[#262626] text-white overflow-hidden">
    
    <nav class="text-center w-full md:w-80 p-6 bg-[#262626] border-b md:border-b-0 md:border-r border-white/10 flex flex-col gap-8 z-20">
        <div>
            <h1 class="text-xl font-bold font-mono tracking-tighter text-blue-400">DRONE VIEWER</h1>
            <p class="text-[8px] sm:text-[10px] font-mono opacity-50">Powered by: Sveltekit + P5.js</p>
        </div>

        <div class="flex flex-row md:flex-col gap-3 md:gap-6 justify-center items-center">
            <div class="grid grid-cols-3 gap-2 mx-auto select-none">
                <button 
                    onpointerdown={() => direction = "up"}
                    onpointerup={() => direction = null}
                    class="col-start-2 w-12 h-12 sm:w-14 sm:h-14 bg-white/5 border border-white/10 rounded-xl"
                >▲</button>
                <button 
                    onpointerdown={() => direction = "left"}
                    onpointerup={() => direction = null}
                    class="col-start-1 row-start-2 w-12 h-12 sm:w-14 sm:h-14 bg-white/5 border border-white/10 rounded-xl"
                >◀</button>
                <button 
                    onpointerdown={() => direction = "right"}
                    onpointerup={() => direction = null}
                    class="col-start-3 row-start-2 w-12 h-12 sm:w-14 sm:h-14 bg-white/5 border border-white/10 rounded-xl"
                >▶</button>
                <button 
                    onpointerdown={() => direction = "down"}
                    onpointerup={() => direction = null}
                    class="col-start-2 row-start-3 w-12 h-12 sm:w-14 sm:h-14 bg-white/5 border border-white/10 rounded-xl"
                >▼</button>
            </div>

            <div class="flex flex-row gap-2 mx-auto select-none">
                <button 
                    onpointerdown={() => zoom = "in"}
                    onpointerup={() => zoom = null}
                    class="w-10 h-10 sm:w-14 sm:h-14 bg-white/5 border border-white/10 rounded-xl"
                >+</button>
                <button 
                    onpointerdown={() => zoom = "out"}
                    onpointerup={() => zoom = null}
                    class="w-10 h-10 sm:w-14 sm:h-14 bg-white/5 border border-white/10 rounded-xl"
                >-</button>
            </div>
            
            <div class="flex flex-col items-center gap-3">
                <span class="text-[10px] font-mono uppercase tracking-widest opacity-60">Model Select</span>
                
                <label class="relative inline-flex items-center cursor-pointer group">
                    <input 
                        type="checkbox" 
                        class="sr-only peer" 
                        onchange={(e) => changeModel(e)}
                    >
                    
                    <div class="w-14 h-7 bg-white/5 border border-white/10 rounded-full peer 
                                peer-checked:bg-blue-500/20 peer-checked:border-blue-400/50 
                                transition-all duration-300 ease-in-out">
                    </div>
                    
                    <div class="absolute left-1 top-1 w-5 h-5 bg-white/40 rounded-full transition-all duration-300 
                                peer-checked:translate-x-7 peer-checked:bg-blue-400 shadow-[0_0_10px_rgba(96,165,250,0)]
                                peer-checked:shadow-[0_0_15px_rgba(96,165,250,0.6)]">
                    </div>
                </label>
                
                <div class="flex gap-4 text-[10px] font-mono mt-1">
                    <span class={selectedModel === 'one' ? 'text-blue-400' : 'opacity-30'}>M-01</span>
                    <span class={selectedModel === 'two' ? 'text-blue-400' : 'opacity-30'}>M-02</span>
                </div>
            </div>
        </div>



        <hr class="border-white/10" />

        <div class="flex items-center justify-center">
            <a 
                href={resolve("/")} 
                class="w-full py-3 px-4 
                border border-white/20 rounded-lg 
                text-white font-mono text-sm hover:bg-white/20 hover:text-black/20 transition-all active:scale-95"
            >
                Regresar al menu
            </a>
        </div>
        
    </nav>

    <section class="relative grow h-full bg-[#1a1a1a]">
        <div class="absolute inset-0 w-full h-full">
            <Sketch {selectedModel} {bg} {direction} {zoom} />
        </div>
        
        <div class="absolute bottom-6 right-6 pointer-events-none border-r-2 border-b-2 border-blue-500/30 w-12 h-12"></div>
        <div class="absolute top-6 left-6 pointer-events-none border-l-2 border-t-2 border-blue-500/30 w-12 h-12"></div>
    </section>

</main>

<style>
    /* Aseguramos que el body no tenga scroll para que el layout se sienta como una App */
    /* :global(body) {
        margin: 0;
        padding: 0;
        overflow: hidden;
    } */
</style>