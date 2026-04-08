<script>
    import { resolve } from "$app/paths";
    import Navbar from "$lib/components/navbar.svelte";

    const currentYear = () => new Date().getFullYear();

</script>
<section class="relative h-screen w-full overflow-hidden bg-black text-white font-sans uppercase tracking-tighter p-6 md:p-10">
  
    <div class="absolute inset-0 z-0 opacity-40">
        <img src="/drone2-tools.png" alt="BG" class="h-full w-full object-cover" />
        <div class="absolute inset-0 flex items-center justify-center pointer-events-none opacity-40">
            <div class="absolute w-full h-px bg-white"></div>
            <div class="absolute h-full w-px bg-white"></div>
        </div>
    </div>

    <div class="relative z-10 h-full w-full flex flex-col justify-between">
        
        <Navbar>
            
        </Navbar>

        <div class="flex justify-between items-center w-full">
            <span class="text-sm font-bold tracking-wide">PROYECTO FIN DE CURSO 2026</span>
            <p class="text-[10px] md:text-xs  leading-tight text-right tracking-widest opacity-80">
                SISTEMAS<br/>ELECTRÓNICA<br/>Y DISEÑO
            </p>
        </div>

        <div class="flex flex-col w-full mb-4">
        
        <div class="flex flex-col sm:flex-row justify-between items-start sm:items-baseline w-full border-b border-transparent">
            <h1 class="text-2xl sm:text-5xl md:text-6xl lg:text-7xl font-black leading-none tracking-tighter">
                DE LA IDEA
            </h1>
            <button class="text-[10px] md:text-sm border-b border-white/40 pb-8 mt-2 sm:mt-0 tracking-widest hover:border-white whitespace-nowrap">
                CONOCE EL PROCESO →
            </button>
        </div>

        <div class="flex flex-col-reverse sm:flex-row justify-between items-start sm:items-baseline w-full -mt-2 sm:-mt-4 md:-mt-6">
            <div class="mt-4 sm:mt-0">
                <p class="text-[10px] md:text-sm leading-tight tracking-[0.2em] font-bold opacity-70">
                    AÑOS DE APRENDIZAJE<br/>MATERIALIZADOS
                </p>
            </div>
            <h1 class="text-2xl sm:text-5xl md:text-6xl lg:text-7xl font-black leading-none tracking-tighter">
                AL PRODUCTO
            </h1>
        </div>
        
        </div>
    </div>
</section>

<section class="relative min-h-screen w-full bg-white text-black font-sans uppercase tracking-wide p-6 md:p-10 md:px-14 overflow-hidden">

    <div class="absolute inset-0 pointer-events-none">
        <div class="absolute top-[37%] left-0 w-full h-px bg-black/10"></div>
        
        <div class="grid grid-cols-2 md:grid-cols-4 h-full px-6 md:px-14">
            <div class="relative z-10 border-r border-black/10"> <!-- Linea que llega hasta el final -->
                <!-- Circulo del puntero -->
                <div class="absolute top-[37%] right-0 -translate-y-1/2 translate-x-1/2 z-20">
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
            ESTE PROYECTO RECORRE LAS ETAPAS CLAVE DE LA CARRERA: DESDE EL DISEÑO ELECTRÓNICO Y 
            LA PROGRAMACIÓN DE MICROCONTROLADORES, HASTA LA DOCUMENTACIÓN VISUAL Y FOTOGRÁFICA. 
            CADA COMPONENTE REFLEJA HORAS DE LABORATORIO, AJUSTES Y VALIDACIÓN.
        </div>

        <div class="flex justify-between items-end w-full mt-24 mb-4">
            <span></span>
            <p class="text-xs md:text-sm font-bold leading-tight text-right tracking-widest opacity-80">
                ETAPAS DEL <br/> DESARROLLO
            </p>
        </div>
    </div>

    <div class="relative z-10 grid grid-cols-2 md:grid-cols-4 ">
        <div class="relative border-r border-b border-black/10 md:border-b-0 p-10 md:pt-32 min-h-56 md:min-h-75">
            <div class="mb-6">
                <img src="/drone-brick-bg.png" class="w-32 md:w-40 -rotate-6 shadow-lg" alt="Un Drone volando frente una pared de ladrillos">
            </div>
            <span class="block text-xl md:text-2xl font-bold">
                0.1
            </span>
            <p class="text-xs md:text-sm font-bold leading-tight uppercase">
                DISEÑO Y<br/>SIMULACIÓN
            </p>
        </div>

        <div class="relative border-b border-black/10 md:border-b-0 md:border-r p-10 md:pt-16">
            <span class="block text-xl md:text-2xl font-bold">
                0.2

            </span>
            <p class="text-xs md:text-sm font-bold leading-tight uppercase">
                PROTOTIPADO<br/>ELECTRÓNICO
            </p>
        </div>

        <div class="relative border-r border-black/10 p-10 pt-16 md:pt-48">
            <span class="block text-xl md:text-2xl font-bold">
                0.3
            </span>
            <p class="text-xs md:text-sm font-bold leading-tight uppercase">
                FOTOGRAFÍA<br/>TÉCNICA
            </p>
        </div>

        <div class="relative border-l border-b border-black/10 md:border-b-0 p-10 md:pt-32 min-h-56 md:min-h-75">
            <div class="mb-6">
                <img src="/drone-UM-bg.png" class="w-32 md:w-40 rotate-6 shadow-lg" alt="Pruebas">
            </div>
            <span class="block text-xl md:text-2xl font-bold">
                0.4
            </span>
            <p class="text-xs md:text-sm font-bold leading-tight uppercase">
                VALIDACIÓN Y<br/>RESULTADOS
            </p>
        </div>
    </div>

</section>


<section id="about" class="relative min-h-screen w-full bg-zinc-900 text-white font-sans uppercase overflow-hidden p-6 md:p-10">
  
    <div class="absolute inset-0 z-0">
        <img src="drone2-leaves.png" alt="Laboratorio" class="h-full w-full object-cover opacity-60" />
    </div>

    <div class="relative z-10 grid grid-cols-1 md:grid-cols-2 h-full min-h-[80vh]">
        
        <div class="flex flex-col justify-center p-4 md:p-12">
            <div class="max-w-md">
                <h2 class="text-2xl md:text-3xl font-black tracking-tighter mb-4">
                    El recorrido
                </h2>
                <p class="text-xs md:text-sm leading-relaxed tracking-widest opacity-90 font-medium">
                    Este proyecto nace de la necesidad de integrar los conocimientos adquiridos 
                    durante la carrera: electrónica analógica y digital, control, procesamiento 
                    de señales, y también la comunicación visual de resultados a través de la 
                    fotografía y el diseño.
                </p>
            </div>
        </div>

        <div class="relative flex flex-col justify-around items-center sm:items-end p-4 md:p-12 space-y-12 md:space-y-0">

            <div class="relative z-10 text-center sm:text-right group">
                <p class="text-[10px] md:text-xs font-bold tracking-[0.2em] mb-1 opacity-70">Fase 1</p>
                <h3 class="text-sm md:text-lg font-black tracking-tighter">Concepto y Diseño</h3>
            </div>

            <div class="relative z-10 text-right max-w-50">
                <h3 class="text-sm md:text-lg font-black tracking-tighter leading-none">
                Desarrollo <br/> en Laboratorio
                </h3>
            </div>

            <div class="relative z-10 text-right">
                <h3 class="text-sm md:text-lg font-black tracking-tighter">
                Documentación <br/> y Fotografía
                </h3>
            </div>

        </div>
    </div>

    <div class="relative z-10 mt-10 p-6 md:p-10 md:absolute md:bottom-12 md:left-12">
        <div class="flex items-center justify-center sm:justify-start gap-4">
            <p class="text-[10px] md:text-xs font-bold tracking-widest hover:text-zinc-400 transition-colors">
                MEMORIA TÉCNICA Y <br/> GALERÍA DE IMÁGENES
            </p>
        </div>
    </div>

</section>


<section class="relative min-h-screen w-full bg-white text-black font-sans uppercase tracking-wide p-6 md:p-10 md:px-14 overflow-hidden flex flex-col justify-center items-center">

    <div class="relative z-10 text-center w-full max-w-6xl">
        
        <!-- Titulo principal -->
        <div class="mb-12 md:mb-16">
            <h2 class="text-3xl sm:text-5xl md:text-6xl lg:text-7xl font-black tracking-tighter leading-none italic">
                EXPLORA LOS <br class="hidden sm:block"/> COMPONENTES DEL PROYECTO
            </h2>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 md:gap-10 w-full">
            
            <!-- Modelo 3D -->
            <div class="group relative border border-black/10 p-6 md:p-8 text-left transition-all duration-300 hover:shadow-2xl hover:border-black/30">
                <div class="absolute -top-1 -left-1 w-3 h-3 border-t-2 border-l-2 border-black/40 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                <div class="absolute -bottom-1 -right-1 w-3 h-3 border-b-2 border-r-2 border-black/40 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                
                <h3 class="text-2xl md:text-3xl font-black tracking-tighter mb-2">
                    Modelos 3D
                </h3>
                <p class="text-xs md:text-sm font-medium tracking-wider text-black/60 mb-6 uppercase">
                    Visualización interactiva de los diseños en tres dimensiones.
                </p>
                
                <a href={resolve("/viewer")} class="relative inline-block group/btn overflow-hidden border border-black/20 px-5 py-2.5 text-[10px] md:text-xs font-black tracking-[0.3em] transition-all duration-300 bg-transparent text-black hover:text-white">
                    <div class="absolute inset-0 bg-black translate-y-full group-hover/btn:translate-y-0 transition-transform duration-300 ease-out"></div>
                    <span class="relative z-10">EXPLORAR</span>
                </a>
            </div>

            <!-- Ficha Tecnica -->
            <div class="group relative border border-black/10 p-6 md:p-8 text-left transition-all duration-300 hover:shadow-2xl hover:border-black/30">
                <div class="absolute -top-1 -left-1 w-3 h-3 border-t-2 border-l-2 border-black/40 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                <div class="absolute -bottom-1 -right-1 w-3 h-3 border-b-2 border-r-2 border-black/40 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                
                <h3 class="text-2xl md:text-3xl font-black tracking-tighter mb-2">
                    Ficha Técnica
                </h3>
                <p class="text-xs md:text-sm font-medium tracking-wider text-black/60 mb-6 uppercase">
                    Especificaciones, y documentación del sistema.
                </p>
                
                <a href={"/fichaTecnica.pdf"} class="relative inline-block group/btn overflow-hidden border border-black/20 px-5 py-2.5 text-[10px] md:text-xs font-black tracking-[0.3em] transition-all duration-300 bg-transparent text-black hover:text-white">
                    <div class="absolute inset-0 bg-black translate-y-full group-hover/btn:translate-y-0 transition-transform duration-300 ease-out"></div>
                    <span class="relative z-10">VER MÁS</span>
                </a>
            </div>

            <!-- Juego -->
            <div class="group relative border border-black/10 p-6 md:p-8 text-left transition-all duration-300 hover:shadow-2xl hover:border-black/30">
                <div class="absolute -top-1 -left-1 w-3 h-3 border-t-2 border-l-2 border-black/40 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                <div class="absolute -bottom-1 -right-1 w-3 h-3 border-b-2 border-r-2 border-black/40 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                
                <h3 class="text-2xl md:text-3xl font-black tracking-tighter mb-2">
                    Juego
                </h3>
                <p class="text-xs md:text-sm font-medium tracking-wider text-black/60 mb-6 uppercase">
                    Una experiencia lúdica que complementa los conceptos del proyecto.
                </p>
                
                <a href={resolve("/game")} class="relative inline-block group/btn overflow-hidden border border-black/20 px-5 py-2.5 text-[10px] md:text-xs font-black tracking-[0.3em] transition-all duration-300 bg-transparent text-black hover:text-white">
                    <div class="absolute inset-0 bg-black translate-y-full group-hover/btn:translate-y-0 transition-transform duration-300 ease-out"></div>
                    <span class="relative z-10">VER MÁS</span>
                </a>
                
            </div>

        </div>
    </div>

</section>




<section class="relative min-h-screen w-full bg-white text-black font-sans uppercase tracking-wide 
    overflow-hidden border-t border-black/10">

    <!-- Líneas de cuadrícula decorativas -->
    <div class="absolute inset-0 pointer-events-none z-0">
        <div class="grid grid-cols-2 md:grid-cols-4 h-full px-6 md:px-14">
            <div class="border-r border-black/10"></div>
            <div class="border-r border-black/10"></div>
            <div class="border-r border-black/10"></div>
        </div>
    </div>

    <div class="relative z-10 max-w-7xl mx-auto h-full min-h-screen flex items-center p-6 md:p-14">

        <div class="grid grid-cols-1 md:grid-cols-2 gap-12 md:gap-16 w-full">
            
            <!-- Columna de texto -->
            <div class="self-center space-y-6 text-center md:text-left">
                
                <h2 class="text-4xl md:text-7xl font-black tracking-tighter text-black">
                    FORMACIÓN <br/> ACADÉMICA
                </h2>
                
                <h3 class="text-2xl sm:text-3xl md:text-5xl font-black tracking-tighter leading-tight">
                    UNIVERSIDAD <br/>
                    <span class="italic pb-1 text-blue-800">
                        UNIVER MILENIUM
                    </span>
                </h3>
                
                <p class="text-xs md:text-sm leading-relaxed tracking-widest font-medium text-black/70 max-w-md mx-auto md:mx-0">
                    Este proyecto fue desarrollado con el apoyo y la formación recibida en la 
                    <strong class="text-black">UNIVERSIDAD UNIVER MILENIUM</strong>, 
                    donde cada etapa desde la conceptualización hasta la validación final 
                    fue guiada por profesionales comprometidos con la excelencia académica y la innovación tecnológica.
                </p>
                
                <a href={resolve("/recognition")} class="relative inline-block group/btn overflow-hidden border border-black/20 px-5 py-2.5 
                text-[10px] md:text-xs font-black tracking-[0.3em] transition-all duration-300 bg-transparent text-black hover:text-white">
                    <div class="absolute inset-0 bg-black translate-y-full group-hover/btn:translate-y-0 transition-transform duration-300 ease-out"></div>
                    <span class="relative z-10">Reconocimientos</span>
                </a>
                
            </div>

            <!-- Columna de video -->
            <div class="h-full w-full overflow-hidden rounded-xl shadow-2xl border border-black">
                <iframe 
                    class="w-full h-full"
                    src="https://www.youtube-nocookie.com/embed/IaqAEzhw3Sg?loop=1&playlist=IaqAEzhw3Sg&controls=1&modestbranding=1&rel=0&showinfo=0&color=white&iv_load_policy=3"
                    title="YouTube video player"
                    frameborder="0"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                    referrerpolicy="strict-origin-when-cross-origin"
                    allowfullscreen
                ></iframe>
            </div>
            
        </div>
    </div>

    <!-- Detalles decorativos -->
    <div class="absolute bottom-6 left-6 md:bottom-10 md:left-10 w-4 h-4 border-b border-l border-black/10"></div>
    <div class="absolute bottom-6 right-6 md:bottom-10 md:right-10 w-4 h-4 border-b border-r border-black/10"></div>
</section>



<section class="relative min-h-screen w-full bg-white text-black font-sans uppercase tracking-wide p-6 md:p-14 overflow-hidden border-t border-black/10">
    
    <div class="absolute inset-0 pointer-events-none">
        <div class="grid grid-cols-2 md:grid-cols-4 h-full px-6 md:px-14">
            <div class="border-r border-black/5"></div>
            <div class="border-r border-black/5"></div>
            <div class="border-r border-black/5"></div>
        </div>
    </div>

    <div class="relative z-10">
        <div class="flex flex-col md:flex-row justify-between items-start md:items-end w-full mb-20">
            
            <h2 class="text-4xl md:text-7xl font-black tracking-tighter ">
                CAMPOS DE <br/> APLICACIÓN
            </h2>
            
            <p class="text-[10px] md:text-xs font-bold leading-tight tracking-[0.2em] opacity-40 mt-8 md:mt-0 md:text-right border-l md:border-l-0 md:border-r-2 border-black pl-4 md:pl-0 md:pr-4">
                POTENCIAL DE INTEGRACIÓN <br/> MULTIDISCIPLINARIA
            </p>
            
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-0 border-t-2 border-black">
            
            <div class="border-b border-black md:border-r md:border-b-0 p-8 md:p-16 hover:bg-white transition-colors duration-500">
                <div class="flex items-center gap-4 mb-16">
                    <span class="text-xs font-black bg-black text-white px-2 py-1">01</span>
                    <span class="text-xs font-black tracking-[0.5em] opacity-50">ACADÉMICO</span>
                </div>
                
                <div class="space-y-12">
                    <div class="group">
                        <h4 class="text-sm font-black italic mb-3 flex items-center gap-2">
                            <span class="w-1.5 h-1.5 bg-black rounded-full opacity-0 group-hover:opacity-100 transition-opacity"></span>
                            DISEÑO GRÁFICO
                        </h4>
                        <p class="text-sm normal-case opacity-60 leading-relaxed max-w-sm">
                            Exploración de ángulos cinemáticos complejos para contenido 3D y generación de narrativa visual técnica de alta fidelidad.
                        </p>
                    </div>
                    
                    <div class="group">
                        <h4 class="text-sm font-black italic mb-3 flex items-center gap-2">
                            <span class="w-1.5 h-1.5 bg-black rounded-full opacity-0 group-hover:opacity-100 transition-opacity"></span>
                            CRIMINOLOGÍA
                        </h4>
                        <p class="text-sm normal-case opacity-60 leading-relaxed max-w-sm">
                            Modelado de precisión para reconstrucción de escenas y análisis perimetral sin alteración de evidencia física.
                        </p>
                    </div>
                    
                    <div class="group">
                        <h4 class="text-sm font-black italic mb-3 flex items-center gap-2">
                            <span class="w-1.5 h-1.5 bg-black rounded-full opacity-0 group-hover:opacity-100 transition-opacity"></span>
                            DERECHO
                        </h4>
                        <p class="text-sm normal-case opacity-60 leading-relaxed max-w-sm">
                            Casos de estudio sobre privacidad de datos, legislación de espacio aéreo y propiedad intelectual en hardware libre.
                        </p>
                    </div>
                </div>
            </div>

            <div class="p-8 md:p-16 md:pt-40 hover:bg-white transition-colors duration-500 flex flex-col justify-between">
                <div>
                    <div class="flex items-center gap-4 mb-16">
                        <span class="text-xs font-black border border-black px-2 py-1">02</span>
                        <span class="text-xs font-black tracking-[0.5em] opacity-50">COMERCIAL</span>
                    </div>
                    
                    <div class="space-y-12">
                        <div class="group">
                            <h4 class="text-sm font-black italic mb-3 flex items-center gap-2">
                                <span class="w-1.5 h-1.5 bg-black rounded-full opacity-0 group-hover:opacity-100 transition-opacity"></span>
                                INSPECCIÓN TÉCNICA
                            </h4>
                            <p class="text-sm normal-case opacity-60 leading-relaxed max-w-sm">
                                Auditoría visual de infraestructuras críticas (puentes, cableado, techumbres) reduciendo costos operacionales y riesgos.
                            </p>
                        </div>
                        
                        <div class="group">
                            <h4 class="text-sm font-black italic mb-3 flex items-center gap-2">
                                <span class="w-1.5 h-1.5 bg-black rounded-full opacity-0 group-hover:opacity-100 transition-opacity"></span>
                                DIGITAL ASSETS
                            </h4>
                            <p class="text-sm normal-case opacity-60 leading-relaxed max-w-sm">
                                Creación de librerías visuales para VFX y publicidad, integrando hardware real en entornos virtuales.
                            </p>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </div>
</section>


<footer id="faq" class="relative flex flex-col justify-between min-h-[70vh] w-full bg-[#1a2315] text-white font-sans uppercase overflow-hidden p-6 md:p-14">
    
    <div class="grid grid-cols-1 md:grid-cols-2 pt-10 pb-20">
        
        <div class="flex items-start md:pl-8 mb-10 md:mb-0">
            <h2 class="text-4xl md:text-5xl font-black tracking-tighter">
                PREGUNTAS <br/> FRECUENTES
            </h2>
        </div>

        <div class="space-y-0.5 border-l border-white/20 md:border-l-0">
            
            <details class="group border-b border-white/20">
                <summary class="flex items-center justify-between py-5 px-6 cursor-pointer list-none hover:bg-white/5 transition-colors">
                    <span class="text-xs md:text-sm font-bold tracking-[0.15em]">
                        ¿Cuál fue el punto de partida del proyecto?
                    </span>
                    <span class="text-xl md:text-2xl font-light transition-transform duration-300 group-open:rotate-90 group-hover:translate-x-2" aria-hidden="true">→</span>
                </summary>
                <div class="px-6 pb-6 text-xs tracking-widest leading-relaxed opacity-70 normal-case">
                    El proyecto comenzó con la necesidad de aplicar los fundamentos de electrónica, control y procesamiento de señales en un sistema funcional, documentando cada etapa.
                </div>
            </details>

            <details class="group border-b border-white/20">
                <summary class="flex items-center justify-between py-5 px-6 cursor-pointer list-none hover:bg-white/5 transition-colors">
                    <span class="text-xs md:text-sm font-bold tracking-[0.15em]">
                        ¿Qué herramientas de diseño y simulación se utilizaron?
                    </span>
                    <span class="text-xl md:text-2xl font-light transition-transform duration-300 group-open:rotate-90 group-hover:translate-x-2" aria-hidden="true">→</span>
                </summary>
                <div class="px-6 pb-6 text-xs tracking-widest leading-relaxed opacity-70 normal-case">
                    Se emplearon software de simulación de circuitos (SPICE) y entornos de desarrollo para microcontroladores como ESP32 y Arduino.
                </div>
            </details>

            <details class="group border-b border-white/20">
                <summary class="flex items-center justify-between py-5 px-6 cursor-pointer list-none hover:bg-white/5 transition-colors">
                    <span class="text-xs md:text-sm font-bold tracking-[0.15em]">
                        ¿Cómo se documentó el proceso?
                    </span>
                    <span class="text-xl md:text-2xl font-light transition-transform duration-300 group-open:rotate-90 group-hover:translate-x-2" aria-hidden="true">→</span>
                </summary>
                <div class="px-6 pb-6 text-xs tracking-widest leading-relaxed opacity-70 normal-case">
                    Se llevó un registro fotográfico detallado de las etapas de construcción, pruebas y resultados, además de bitácoras técnicas y esquemáticos.
                </div>
            </details>

            <details class="group border-b border-white/20">
                <summary class="flex items-center justify-between py-5 px-6 cursor-pointer list-none hover:bg-white/5 transition-colors">
                    <span class="text-xs md:text-sm font-bold tracking-[0.15em]">
                        ¿Qué materias de la carrera se integraron?
                    </span>
                    <span class="text-xl md:text-2xl font-light transition-transform duration-300 group-open:rotate-90 group-hover:translate-x-2" aria-hidden="true">→</span>
                </summary>
                <div class="px-6 pb-6 text-xs tracking-widest leading-relaxed opacity-70 normal-case">
                    Electrónica analógica y digital, sistemas embebidos, programación avanzada, diseño web y gestión de proyectos.
                </div>
            </details>

            <details class="group border-b border-white/20">
                <summary class="flex items-center justify-between py-5 px-6 cursor-pointer list-none hover:bg-white/5 transition-colors">
                    <span class="text-xs md:text-sm font-bold tracking-[0.15em]">
                        ¿Dónde se pueden ver más detalles?
                    </span>
                    <span class="text-xl md:text-2xl font-light transition-transform duration-300 group-open:rotate-90 group-hover:translate-x-2" aria-hidden="true">→</span>
                </summary>
                <div class="px-6 pb-6 text-xs tracking-widest leading-relaxed opacity-70 normal-case">
                    Toda la documentación y planos están disponibles en las secciones habilitadas en este sitio.
                </div>
            </details>

        </div>
    </div>

    <div class="border-t border-white/20 pt-10 pb-4">
        <div class="flex flex-col sm:flex-row justify-between items-start sm:items-center gap-6">
        
        <div class="text-sm md:text-base font-extrabold tracking-[0.3em]">
            PROYECTO DE FIN DE CURSO 2026
        </div>

        <nav class="flex flex-wrap gap-x-6 gap-y-2 text-[10px] md:text-xs font-bold tracking-[0.2em] opacity-80">
            <a href="#" class="hover:text-white hover:opacity-100 transition-opacity">Inicio</a>
            <!-- <a href="#" class="hover:text-white hover:opacity-100 transition-opacity">Proceso</a>
            <a href="#" class="hover:text-white hover:opacity-100 transition-opacity">Galería</a>
            <a href="#" class="hover:text-white hover:opacity-100 transition-opacity">FAQ</a>
            <a href="#" class="hover:text-white hover:opacity-100 transition-opacity">Contacto</a> -->
        </nav>
        
        </div>
    </div>

</footer>

<style>
    /* Oculta la flecha por defecto de la etiqueta summary en navegadores */
    summary::-webkit-details-marker {
        display: none;
    }
</style>