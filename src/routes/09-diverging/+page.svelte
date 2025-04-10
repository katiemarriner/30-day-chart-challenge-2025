<script>
  import { onMount } from "svelte";
  import { scaleLinear, scaleOrdinal } from 'd3-scale';

  let data;
  onMount(async () => {
    const res = await fetch('09-diverging.json');
    data = await res.json();
  });
  
  $: console.log(data)
</script>

<!-- for each country create a div that will hold an svg pyramid chart -->
<!-- base line is half of the width, vertical axis is ordinal, horizontal is linear -->