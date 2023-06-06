<script>
    let counter = 15;
    let x = Math.round();
    let y = 15;
    let z;

    $: z = x + y;
    function increase() {
        counter++;
    }

    const decrese = () => {
        counter--;
    };
</script>

<svelte>
    <title>Slender never gets tired</title>
</svelte>
<h1 class="bg-blue-600">Kalcata</h1>

<input type="number" bind:value={x} />
+
<input type="number" bind:value={y} />
=
<input type="number" bind:value={z} readonly />

<h1>Hello, Hood!</h1>
<p>And the count is: {counter}</p>
<button on:click={increase} class="bg-blue-200">+</button>
<button on:click={decrese}>-</button>

<style>
    h1 {
        color: #909090;
    }
</style>
