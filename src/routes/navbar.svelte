<script>
	import Home from '$lib/assets/home.png';
	import Learn from '$lib/assets/learn.png';
	import Post from '$lib/assets/post.png';
	import Explore from '$lib/assets/explore.png';
	import Logo from '$lib/assets/logo.png';
	import Profile from '$lib/assets/profile.png';
	import * as Avatar from '$lib/components/ui/avatar';
	import Button from '$lib/components/ui/button/button.svelte';

	import { ChevronDown } from 'lucide-svelte';
</script>

<div
	class="navbar mx-5 flex items-center justify-between border-b-[1.5px] border-dotted border-[#525C69] pb-4"
>
	<div class="flex items-center gap-2 text-lg xl:text-2xl font-bold">
		<img class="h-4 xl:h-8 w-4 xl:w-8" src={Logo} alt="home" />duggup
	</div>
	<div class="flex items-center justify-between gap-10">
		<ul class="flex gap-2 xl:gap-10">
			<li>
				<Button
					class="flex gap-2 border-0 border-black hover:border-x-[1px] hover:border-b-[4px] hover:border-t-[1px] hover:bg-white"
					variant="outline"><img class="h-6 w-6" src={Home} alt="home" />Home</Button
				>
			</li>
			<li>
				<Button
					class="flex gap-2 border-0 border-black hover:border-x-[1px] hover:border-b-[4px] hover:border-t-[1px] hover:bg-white"
					variant="outline"><img class="h-6 w-6" src={Explore} alt="home" />Explore</Button
				>
			</li>
			<li>
				<Button
					class="flex gap-2 border-0 border-black hover:border-x-[1px] hover:border-b-[4px] hover:border-t-[1px] hover:bg-white"
					variant="outline"><img class="h-6 w-6" src={Learn} alt="home" />Learn</Button
				>
			</li>
			<li>
				<Button
					class="flex gap-2 border-0 border-black hover:border-x-[1px] hover:border-b-[4px] hover:border-t-[1px] hover:bg-white"
					variant="outline"><img class="h-6 w-6" src={Post} alt="home" />Post</Button
				>
			</li>
		</ul>
		<div class="flex items-center gap-2 text-xl">
			<Avatar.Root>
				<Avatar.Image src={Profile} alt="@shadcn" />
				<Avatar.Fallback>CN</Avatar.Fallback>
			</Avatar.Root> Krishna Kiran
			<ChevronDown class="flex h-5 w-5 items-center" />
		</div>
	</div>
</div>
