<script>
    import { onMount } from "svelte";
    import * as d3 from 'd3';
    let tempData = [];

    onMount(async () => {
        const res = await fetch('earthquakes_1992_1994.csv'); 
        const csv = await res.text();
        tempData = d3.csvParse(csv, d3.autoType)
        console.log(tempData);
    });
</script>

<main>
    <h1>TESTING!</h1>
</main>