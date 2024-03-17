<script>
    export let data = [];

    // LIBS
    import { onMount } from 'svelte';

    // COMPONENTS
    import Tooltip from '$components/Tooltip.svelte';

    // VARS
    let tooltipData;
    let width = 500;
    let height = 500;

    const margin = {
		top: 20,
		right: 20,
		bottom: 20,
		left: 20 
	};
    $: console.log(data);

    // FUNCTIONS
    function init() {
        console.log('CHART INIT!')
    }
    function addCommasToNumber(number) {
        return number.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
    }

    // LIGHTS! CAMERA! ACTION!
    onMount(init);
</script>

<pre>{`CHART: Resolved data = ${JSON.stringify(data)}`}</pre>

<div class="chart-container" bind:clientWidth={width}>

</div>