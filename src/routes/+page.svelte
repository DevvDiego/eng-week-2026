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

<section class="relative h-screen w-full bg-white text-black font-sans uppercase tracking-wide p-6 md:p-10 md:px-14">

    <div class="absolute inset-0 z-0 opacity-40">
        <div class="absolute inset-0 flex items-center justify-center pointer-events-none opacity-40">
            <div class="absolute w-full h-px bg-neutral-950"></div>
            <div class="absolute left-1/5 h-full w-px bg-neutral-950"></div>
        </div>
    </div>

    <div class="text-lg sm:text-xl text-center font-semibold mt-5 ">
        MIRANDO AL MUNDO DESDE OTRA PERSPECTIVA: MÁS QUE UN PROYECTO, ES EL RESULTADO DE MILES DE ITERACIONES, 
        PRUEBAS Y CÁLCULOS. DOCUMENTAMOS EL CAMINO RECORRIDO PARA DOMINAR LA TECNOLOGÍA AÉREA, 
        CONSOLIDANDO LOS PILARES DE LA INGENIERÍA MODERNA EN UNA ESTRUCTURA CAPAZ DE DESAFIAR LA GRAVEDAD.    
    </div>

    <div class="flex justify-between items-center w-full mt-40">
        <span></span>
        <p class="text-[10px] md:text-xs leading-tight text-right tracking-widest opacity-80">
            ¿Que ingenieria <br/> hay detras <br/> de todo?
        </p>
    </div>

</section>