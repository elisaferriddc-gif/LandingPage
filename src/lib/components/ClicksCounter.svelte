<!--Props sonovariabili che passi da un componente padre a uno figlio-->
<script>
 let {
    initialCount: count=$bindable(0),
    willIncrement = () => {},
    didIncrement = () => {}
 } = $props() 

 let doubled = $derived(count * 2);

const increment = () => {
    willIncrement(count)
    count++
    didIncrement(count)
}
</script>

<h1>Click Counter</h1>

<button onclick={increment}>
    clicks: {count}
</button>

<!--<button onclick={() => count++}> Questa la uso quando non ho increment e il callback-->
    <!--clicks: {count}-->
<!--</button>-->

<span>
    doubled is {doubled}
</span>
