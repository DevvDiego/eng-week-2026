<script lang="ts">
    import { resolve } from '$app/paths';

</script>

<header class="flex justify-between items-start  font-sans uppercase tracking-tighter">
	<h2 class="text-lg font-bold italic tracking-normal">Quetza - les</h2>
	
	<nav class="flex gap-6 sm:gap-10 text-xs tracking-widest">
		<a href={resolve("/")} class="hover:opacity-50">MAIN</a>
		<a href="#about" class="hover:opacity-50">ABOUT</a>
		<!-- <a href="" class="hover:opacity-50">STORE</a>
		<a href="" class="hover:opacity-50">CONTACT</a> -->
	</nav>

</header>