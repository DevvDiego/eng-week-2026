<script>
  import Sketch from '$lib/components/sketch.svelte';
  let bg = "#262626";
  let color = '#00d8ff';
</script>

<h1>3D model viewer test</h1>

<div class="controls">
  <h1>background</h1>
  <input type="color" bind:value={bg} />
  
  <h1>fill color</h1>
  <input type="color" bind:value={color} />
</div>

<Sketch {bg} {color} />