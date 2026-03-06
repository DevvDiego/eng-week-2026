<script>
    import Navbar from "$lib/components/navbar.svelte";

    const currentYear = () => new Date().getFullYear();

</script>
<section class="relative h-screen w-full overflow-hidden bg-black text-white font-sans uppercase tracking-tighter p-6 md:p-10">
  
  <div class="absolute inset-0 z-0 opacity-40">
    <img src="https://picsum.photos/id/10/2500/1600" alt="BG" class="h-full w-full object-cover" />
    <div class="absolute inset-0 flex items-center justify-center pointer-events-none opacity-40">
      <div class="absolute w-full h-px bg-white"></div>
      <div class="absolute h-full w-px bg-white"></div>
    </div>
  </div>

  <div class="relative z-10 h-full w-full flex flex-col justify-between">
    
    <Navbar>
        
    </Navbar>

    <div class="flex justify-between items-center w-full">
      <span class="text-sm font-bold tracking-wide">Engineering week 2026</span>
      <p class="text-[10px] md:text-xs  leading-tight text-right tracking-widest opacity-80">
        Mirando al<br/>mundo desde<br/>otra perspectiva
      </p>
    </div>

    <div class="flex flex-col w-full mb-4">
      
      <div class="flex flex-col sm:flex-row justify-between items-start sm:items-baseline w-full border-b border-transparent">
        <h1 class="text-2xl sm:text-5xl md:text-6xl lg:text-7xl font-black leading-none tracking-tighter">
          TRUE SYSTEMS
        </h1>
        <button class="text-[10px] md:text-sm border-b border-white/40 pb-8 mt-2 sm:mt-0 tracking-widest hover:border-white whitespace-nowrap">
          CHOOSE A MODEL →
        </button>
      </div>

      <div class="flex flex-col-reverse sm:flex-row justify-between items-start sm:items-baseline w-full -mt-2 sm:-mt-4 md:-mt-6">
        <div class="mt-4 sm:mt-0">
          <p class="text-[10px] md:text-sm leading-tight tracking-[0.2em] font-bold opacity-70">
            LA HISTORIA DEL DISEÑO,<br/>PASO A PASO
          </p>
        </div>
        <h1 class="text-2xl sm:text-5xl md:text-6xl lg:text-7xl font-black leading-none tracking-tighter">
          ENGINEERING
        </h1>
      </div>
      
    </div>
  </div>
</section>

<section class="relative min-h-screen w-full bg-white text-black font-sans uppercase tracking-wide p-6 md:p-10 md:px-14 overflow-hidden">

    <div class="absolute inset-0 pointer-events-none">
        <div class="absolute top-[35%] left-0 w-full h-px bg-black/10"></div>
        
        <div class="grid grid-cols-2 md:grid-cols-4 h-full px-6 md:px-14">
            <div class="relative border-r border-black/10">
                <div class="absolute top-[35%] right-0 -translate-y-1/2 translate-x-1/2 z-20">
                    <div class="bg-white border border-black/30 rounded-full w-8 h-8 flex items-center justify-center">
                        <div class="w-4 h-4 border border-black/40 rounded-full flex items-center justify-center relative">
                            <div class="w-px h-full bg-black/40 absolute"></div>
                            <div class="h-px w-full bg-black/40 absolute"></div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="hidden md:block"></div>
            <div class="hidden md:block"></div>
            <div class="hidden md:block"></div>
        </div>
    </div>

    <div class="relative z-10">
        <div class="text-lg sm:text-xl text-center font-semibold mt-5 max-w-5xl mx-auto">
            MIRANDO AL MUNDO DESDE OTRA PERSPECTIVA: MÁS QUE UN PROYECTO, MILES DE ITERACIONES, 
            PRUEBAS Y CÁLCULOS. CONSOLIDANDO LOS PILARES DE LA INGENIERÍA MODERNA 
            EN UNA ESTRUCTURA CAPAZ DE DESAFIAR LA GRAVEDAD.    
        </div>

        <div class="flex justify-between items-end w-full mt-24 mb-4">
            <span></span>
            <p class="text-xs md:text-sm font-bold leading-tight text-right tracking-widest opacity-80">
                ¿QUE INGENIERÍA HAY <br/> DETRÁS DE TODO?
            </p>
        </div>
    </div>

    <div class="relative z-10 grid grid-cols-2 md:grid-cols-4 ">
        <div class="relative border-r border-b border-black/10 md:border-b-0 p-10 md:pt-32 min-h-56 md:min-h-75">
            <div class="mb-6">
                <img src="https://picsum.photos/800" class="w-32 md:w-40 -rotate-6 shadow-lg" alt="Drone">
            </div>
            <span class="block text-xl md:text-2xl font-bold">0.1</span>
            <p class="text-xs md:text-sm font-bold leading-tight uppercase">Cutting-edge<br/>Technology</p>
        </div>

        <div class="relative border-b border-black/10 md:border-b-0 md:border-r p-10 md:pt-16">
            <span class="block text-xl md:text-2xl font-bold">0.2</span>
            <p class="text-xs md:text-sm font-bold leading-tight uppercase">Durable and<br/>Reliable</p>
        </div>

        <div class="relative border-r border-black/10 p-10 pt-16 md:pt-48">
            <span class="block text-xl md:text-2xl font-bold">0.3</span>
            <p class="text-xs md:text-sm font-bold leading-tight uppercase">Competitive<br/>Pricing</p>
        </div>

        <div class="relative border-l border-b border-black/10 md:border-b-0 p-10 md:pt-32 min-h-56 md:min-h-75">
            <div class="mb-6">
                <img src="https://picsum.photos/800" class="w-32 md:w-40 rotate-6 shadow-lg" alt="Drone">
            </div>
            <span class="block text-xl md:text-2xl font-bold">0.1</span>
            <p class="text-xs md:text-sm font-bold leading-tight uppercase">Cutting-edge<br/>Technology</p>
        </div>
    </div>

</section>


<section class="relative min-h-screen w-full bg-zinc-900 text-white font-sans uppercase overflow-hidden p-6 md:p-10">
  
    <div class="absolute inset-0 z-0">
        <img src="https://picsum.photos/id/1081/1200/1800" alt="Aerial View" class="h-full w-full object-cover opacity-60" />
    </div>

    <div class="relative z-10 grid grid-cols-1 md:grid-cols-2 h-full min-h-[80vh]">
        
        <div class="flex flex-col justify-center p-4 md:p-12">
            <div class="max-w-md">
                <h2 class="text-2xl md:text-3xl font-black tracking-tighter mb-4">
                    Nuestra mision
                </h2>
                <p class="text-xs md:text-sm leading-relaxed tracking-widest opacity-90 font-medium">
                    To empower individuals and businesses with cutting-edge drone technology, 
                    providing exceptional products and services that exceed expectations.
                </p>
            </div>
        </div>

        <div class="relative flex flex-col justify-around items-end p-4 md:p-12 space-y-12 md:space-y-0">

            <div class="relative z-10 text-right group">
                <p class="text-[10px] md:text-xs font-bold tracking-[0.2em] mb-1 opacity-70">Adrenaline-pumping</p>
                <h3 class="text-sm md:text-lg font-black tracking-tighter">Drone Racing</h3>
            </div>

            <div class="relative z-10 text-right max-w-50">
                <h3 class="text-sm md:text-lg font-black tracking-tighter leading-none">
                Push the limits of <br/> drone performance
                </h3>
            </div>

            <div class="relative z-10 text-right">
                <h3 class="text-sm md:text-lg font-black tracking-tighter">
                Race to the <br/> finish line
                </h3>
            </div>

        </div>
    </div>

    <div class="relative z-10 mt-10 md:absolute md:bottom-12 md:left-12">
        <div class="flex items-center gap-4">
            <p class="text-[10px] md:text-xs font-bold tracking-widest hover:text-zinc-400 transition-colors">
                JOIN THE DRONE <br/> RACING REVOLUTION
            </p>
        </div>
    </div>

</section>

<!-- <section class="relative h-screen w-full overflow-hidden bg-black text-white font-sans uppercase tracking-tighter p-6 md:p-10">
  
  <div class="absolute inset-0 z-0 opacity-40">
    <img src="https://picsum.photos/id/1/2500/1600" alt="BG" class="h-full w-full object-cover" />
    <div class="absolute inset-0 flex items-center justify-center pointer-events-none opacity-40">
      <div class="absolute w-full h-px bg-white"></div>
      <div class="absolute h-full w-px bg-white"></div>
    </div>
  </div>

  <div class="relative z-10 h-full w-full flex flex-col justify-between">
    
    <Navbar>
        
    </Navbar>

    <div class="flex justify-between items-center w-full">
      <span class="text-sm font-bold tracking-wide">Engineering week 2026</span>
      <p class="text-[10px] md:text-xs  leading-tight text-right tracking-widest opacity-80">
        Mirando al<br/>mundo desde<br/>otra perspectiva
      </p>
    </div>

    <div class="flex flex-col w-full mb-4">
      
      <div class="flex flex-col sm:flex-row justify-between items-start sm:items-baseline w-full border-b border-transparent">
        <h1 class="text-2xl sm:text-5xl md:text-6xl lg:text-7xl font-black leading-none tracking-tighter">
          TRUE SYSTEMS
        </h1>
        <button class="text-[10px] md:text-sm border-b border-white/40 pb-8 mt-2 sm:mt-0 tracking-widest hover:border-white whitespace-nowrap">
          CHOOSE A MODEL →
        </button>
      </div>

      <div class="flex flex-col-reverse sm:flex-row justify-between items-start sm:items-baseline w-full -mt-2 sm:-mt-4 md:-mt-6">
        <div class="mt-4 sm:mt-0">
          <p class="text-[10px] md:text-sm leading-tight tracking-[0.2em] font-bold opacity-70">
            LA HISTORIA DEL DISEÑO,<br/>PASO A PASO
          </p>
        </div>
        <h1 class="text-2xl sm:text-5xl md:text-6xl lg:text-7xl font-black leading-none tracking-tighter">
          ENGINEERING
        </h1>
      </div>
      
    </div>
  </div>
</section> -->