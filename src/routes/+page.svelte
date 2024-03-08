<script lang="ts">
	import Navbar from './navbar.svelte';
	import Timeline from './timeline.svelte';
	import { Pickaxe } from 'lucide-svelte';

	import { onMount } from "svelte";
  import { Progress } from "$lib/components/ui/progress/index.js";
 
  let value = 13;
  onMount(() => {
    const timer = setTimeout(() => (value = 66), 500);
    return () => clearTimeout(timer);
  });
</script>

<div class="hidden lg:block xl:mx-10">
	<Navbar />
	<Timeline />
</div>

<div class="lg:hidden my-10">
	<div class="flex gap-4 mb-5">
		Work in Progress <Pickaxe />
	</div>
	<Progress {value} max={100} class="w-[60%]" />
</div>
