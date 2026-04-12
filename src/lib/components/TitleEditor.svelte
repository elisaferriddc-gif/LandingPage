<!-- Per aggiornare in modo globale il titolo della pagina--> 
<script> 
import { website } from "$lib/state.svelte.js"; 
</script>

<h3>Title Editor</h3>

<input type="text" bind:value={website.title} /> <!-- scrivendo nell'input il titolo del sito cambia-->