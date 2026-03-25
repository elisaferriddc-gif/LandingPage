<script>
 console.log('Hello from SvelteKit!');   
 let count = $state(2);
 let doubled = $derived(count * 2);
</script>

<h1>Click Counter</h1>

<button onclick={() => count++}>
    clicks: {count}
</button>

<span>
    doubled: {doubled}
</span>