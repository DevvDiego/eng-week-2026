<script>
    import Navbar from "$lib/components/navbar.svelte";

</script>
<section class="relative h-screen w-full overflow-hidden bg-black text-white font-sans uppercase tracking-tighter p-6 md:p-10">
  
  <div class="absolute inset-0 z-0 opacity-40">
    <img src="https://picsum.photos/id/10/2500/1600" alt="BG" class="h-full w-full object-cover" />
    <div class="absolute inset-0 flex items-center justify-center pointer-events-none opacity-20">
      <div class="absolute w-full h-px bg-white"></div>
      <div class="absolute h-full w-px bg-white"></div>
    </div>
  </div>

  <div class="relative z-10 h-full w-full flex flex-col justify-between">
    
    <Navbar>
        
    </Navbar>

    <div class="flex justify-between items-center w-full">
      <span class="text-sm font-bold">2023</span>
      <p class="text-[10px] md:text-xs  leading-tight text-right tracking-widest opacity-80">
        CAPTURE THE<br/>WORLD FROM A<br/>NEW PERSPECTIVE
      </p>
    </div>

    <div class="flex flex-col w-full mb-4">
      
      <div class="flex flex-col sm:flex-row justify-between items-start sm:items-baseline w-full border-b border-transparent">
        <h1 class="text-2xl sm:text-5xl md:text-6xl lg:text-7xl font-black leading-none tracking-tighter">
          EXPERIENCE THE
        </h1>
        <button class="text-[10px] md:text-sm border-b border-white/40 pb-8 mt-2 sm:mt-0 tracking-widest hover:border-white whitespace-nowrap">
          CHOOSE A MODEL →
        </button>
      </div>

      <div class="flex flex-col-reverse sm:flex-row justify-between items-start sm:items-baseline w-full -mt-2 sm:-mt-4 md:-mt-6">
        <div class="mt-4 sm:mt-0">
          <p class="text-[10px] md:text-sm leading-tight tracking-[0.2em] font-bold opacity-70">
            YOUR STORY,<br/>TOLD FROM ABOVE
          </p>
        </div>
        <h1 class="text-2xl sm:text-5xl md:text-6xl lg:text-7xl font-black leading-none tracking-tighter">
          FUTURE OF FLIGHT
        </h1>
      </div>
      
    </div>
  </div>
</section>