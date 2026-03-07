<script lang="ts">
    import { resolve } from '$app/paths';
  import Sketch from '$lib/components/sketch.svelte';

  let bg = "#262626";
  let direction: null|String = $state(null);
</script>

<main class="flex flex-col-reverse md:flex-row w-full h-screen bg-[#262626] text-white overflow-hidden">
    
    <nav class="text-center w-full md:w-80 p-6 bg-[#262626] border-b md:border-b-0 md:border-r border-white/10 flex flex-col gap-8 z-20">
        <div>
            <h1 class="text-xl font-bold font-mono tracking-tighter text-blue-400">DRONE VIEWER</h1>
            <p class="text-[8px] sm:text-[10px] font-mono opacity-50">Powered by: Sveltekit + P5.js</p>
        </div>

        <div class="grid grid-cols-3 gap-2 mx-auto select-none">
            <button 
                onpointerdown={() => direction = "up"}
                onpointerup={() => direction = "null"}
                class="col-start-2 w-14 h-14 bg-white/5 border border-white/10 rounded-xl"
            >▲</button>
            <button 
                onpointerdown={() => direction = "left"}
                onpointerup={() => direction = "null"}
                class="col-start-1 row-start-2 w-14 h-14 bg-white/5 border border-white/10 rounded-xl"
            >◀</button>
            <button 
                onpointerdown={() => direction = "right"}
                onpointerup={() => direction = "null"}
                class="col-start-3 row-start-2 w-14 h-14 bg-white/5 border border-white/10 rounded-xl"
            >▶</button>
            <button 
                onpointerdown={() => direction = "down"}
                onpointerup={() => direction = "null"}
                class="col-start-2 row-start-3 w-14 h-14 bg-white/5 border border-white/10 rounded-xl"
            >▼</button>
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
            <Sketch {bg} {direction} />
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