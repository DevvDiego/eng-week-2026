<script lang="ts">
    import { resolve } from '$app/paths';
    
    let {
      class: klass = ""
    } = $props();

</script>

<header class="{klass} flex justify-between items-start  font-sans uppercase tracking-tighter">
	<h2 class="text-lg font-bold italic tracking-normal">
    	<a href={resolve("/")} class="hover:opacity-50">
         Quetza - les
        </a>    
	</h2>
	
	<nav class="flex gap-6 sm:gap-10 text-xs tracking-widest">
    	<a href={resolve("/") + "#about"} class="hover:opacity-50">ABOUT</a>
    	<a href={resolve("/") + "#faq"} class="hover:opacity-50">FAQ</a>
	
		<!-- <a href={resolve("/game")} class="hover:opacity-50">GAME</a>
		<a href={resolve("/viewer")} class="hover:opacity-50">3D MODEL</a>
		<a href={resolve("/recognition")} class="hover:opacity-50">THANKS</a> -->
	</nav>

</header>