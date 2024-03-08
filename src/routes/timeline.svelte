<script>
	import Steve from '$lib/assets/steve.png';
	import Sam from '$lib/assets/sam.png';
	import Logo from '$lib/assets/logo2.png';
	import BetterUp from '$lib/assets/betterup.png';
	import PC from '$lib/assets/pc.png';
	import Image1 from '$lib/assets/image1.png';
	import Icon1 from '$lib/assets/icon1.png';
	import Icon2 from '$lib/assets/icon2.png';
	import * as Avatar from '$lib/components/ui/avatar';
	import Avatar2 from '$lib/assets/avatar.png';
	import Button from '$lib/components/ui/button/button.svelte';
	import { ArrowUpRightFromSquare } from 'lucide-svelte';
	import * as Card from '$lib/components/ui/card';
	import Dots from '$lib/assets/dots.png';
	import { ChevronUp } from 'lucide-svelte';

	let isFollowed = false;

	function toggleFollow() {
		isFollowed = !isFollowed;
	}
</script>

<div class="mx-10 xl:mx-32 mt-16">
	<div
    class="relative xl:space-y-8 before:absolute before:inset-0 before:ml-10 before:h-full before:w-full before:-translate-x-px before:border-[#778FB1] before:border-l-2 before:border-dotted xl:before:ml-[8.55rem] md:before:translate-x-1"
	>
		<div class="relative mb-5 bg-white">
			<div class="mb-20 items-center gap-5 bg-white md:flex md:space-x-4">
				<div class="-ml-24 xl:-ml-8 flex items-start">
					<!-- Icon -->
					<div class="flex flex-col items-end justify-center rounded-full md:order-1">
						<Avatar.Root class="h-20 w-20 xl:h-32 xl:w-32">
							<Avatar.Image src={Avatar2} alt="@shadcn" />
							<Avatar.Fallback>CN</Avatar.Fallback>
						</Avatar.Root>
						<p class="flex w-full justify-center text-xl font-bold text-gray-600">
							Krishna <br /> Kiran
						</p>
					</div>
					<!-- Date -->
					<time class="font-caveat text-xl font-medium text-white md:w-28">Apr 7, 2024</time>
				</div>
				<!-- Title -->
				<div class="flex">
					<div class="flex flex-col gap-5 text-sm xl:text-lg">
						<p>
							Co-Founder and CEO at Duggup - Social network for people in tech. Ex-Amazon Head of
							Engineering. I write hot-takes on building a business, shipping delightful products
							and accelerating product and career growth.
						</p>
						<div>
							<Button
								class="border-x-[0.5px] border-b-[5px] border-black hover:border-0 hover:bg-[#0066FF] hover:text-white"
								variant="outline"
								on:click={toggleFollow}
							>
								{isFollowed ? 'Followed' : 'Follow'}
							</Button>
						</div>
					</div>
					<div class="flex w-60 items-start justify-end">
						<div class=" flex flex-col items-start justify-end">
							<Avatar.Root class="right-0 ml-40 w-6 h-6 xl:w-10 xl:h-10">
								<Avatar.Image class="flex justify-end" src={Logo} alt="@shadcn" />
								<Avatar.Fallback>CN</Avatar.Fallback>
							</Avatar.Root>
							<p class="flex w-full justify-end font-bold">Duggup</p>
							<p class="flex w-full text-xs xl:text-sm justify-end text-slate-500">Co-Founder and CEO</p>
							<a
								href="https://duggup.com/"
								target="_blank"
								class="mt-5 flex w-full text-xs xl:text-sm items-center justify-end gap-1"
							>
								Website <ArrowUpRightFromSquare class="h-4 w-4" />
								<img class="ml-2" src={Dots} alt="dotss " />
							</a>
						</div>
					</div>
				</div>
			</div>
			<!-- <Main/> -->
		</div>

		<!-- Item #1 -->
		<div class="relative">
			<div class=" items-center md:flex md:space-x-4">
				<div class="-ml-24 xl:ml-0 flex items-center space-x-4 md:space-x-2 md:space-x-reverse">
					<div class="ml-3 flex h-4 w-4 items-end justify-center rounded-full md:order-1">
						<img src={Icon2} alt="icon" />
					</div>
					<time class="font-caveat flex justify-end text-xs font-medium text-gray-500 md:w-28"
						>Dec 2023</time
					>
				</div>
				<div class="ml-44">
					<div class="ml-10 flex gap-5">
						<Card.Root class="border-[1px] shadow-sm">
							<Card.Header class="rounded-xl p-0">
								<Card.Title><img src={Steve} alt="steve" /></Card.Title>
							</Card.Header>
							<Card.Content>
								<p class="text-sm mt-5 w-44 xl:w-72">
									No amount of technology can convert a bad story into a good story.
								</p>
							</Card.Content>
						</Card.Root>
						<Card.Root class="border-[1px] shadow-sm">
							<Card.Header class="rounded-xl p-0">
								<Card.Title><img class="rounded-t-xl p-0" src={Sam} alt="steve" /></Card.Title>
							</Card.Header>
							<Card.Content>
								<p class="text-sm mt-5 w-44 xl:w-72">
									Most people don't have original ideas. Here is how Sam Altman pushes himself to
									have unpopular ideas.
								</p>
							</Card.Content>
						</Card.Root>
					</div>
				</div>
			</div>
		</div>

		<div class="relative">
			<div class="">
				<div class="flex">
					<div class="ml-[4%] xl:ml-[10.2%]">
						<ChevronUp class="h-8 w-8 text-[#778FB1]" />
					</div>
				</div>
			</div>
		</div>

		<!-- Item #2 -->
		<div class="relative">
			<div class="mb-3 items-center md:flex md:space-x-4">
				<div class="-ml-24 xl:ml-0 flex items-center">
					<!-- Icon -->
					<div class="ml-2 flex h-6 w-6 items-end justify-center rounded-full md:order-1">
						<img src={Icon1} alt="icon" />
					</div>
					<div
						class="font-caveat -ml-4 flex w-full flex-col justify-end text-xs font-medium text-gray-500"
					>
						<Avatar.Root class="ml-28 xl:ml-24 flex justify-end w-6 h-6 xl:h-10 xl:w-10">
							<Avatar.Image class="flex justify-end" src={Logo} alt="@shadcn" />
							<Avatar.Fallback>CN</Avatar.Fallback>
						</Avatar.Root>
						<p class="flex w-full justify-end text-lg font-bold text-black">Duggup</p>
						<p>San Francisco Bay Area</p>
						<p class="flex justify-end">Joined</p>
						<p class="flex justify-end">Nov 2023</p>
					</div>
				</div>
				<div class="ml-44">
					<div class="ml-10 flex gap-5">
						<Card.Root class="w-[600px] xl:w-[710px] border-0 shadow-md">
							<Card.Header>
								<Card.Title>Co-Founder and CEO</Card.Title>
								<Card.Description>Full-time · Remote</Card.Description>
							</Card.Header>
						</Card.Root>
					</div>
				</div>
			</div>
		</div>

		<!-- Item #3 -->
		<div class="relative">
			<div class="mb-3 items-center md:flex md:space-x-4">
				<div class="-ml-24 xl:ml-0 flex items-center space-x-4 md:space-x-2 md:space-x-reverse">
					<!-- Icon -->
					<div class="ml-3 flex h-4 w-4 items-end justify-center rounded-full md:order-1">
						<img src={Icon2} alt="icon" />
					</div>
					<!-- Date -->
					<time class="font-caveat flex justify-end text-xs font-medium text-gray-500 md:w-28"
						>Dec 2023</time
					>
				</div>
				<div class="ml-44">
					<div class="ml-10 flex gap-5">
						<Card.Root class="border-[1px] shadow-sm">
							<Card.Header class="rounded-xl p-0">
								<Card.Title><img src={PC} alt="steve" /></Card.Title>
							</Card.Header>
							<Card.Content>
								<p class="mt-5 w-44 xl:w-72">
									Startup Lesson I am reflecting. Don't build for the "average person".
								</p>
							</Card.Content>
						</Card.Root>
						<Card.Root class="border-[1px] shadow-sm">
							<Card.Header class="rounded-xl p-0">
								<Card.Title><img src={Image1} alt="steve" /></Card.Title>
							</Card.Header>
							<Card.Content>
								<p class="mt-5 w-44 xl:w-72">Your biggest regrets at 80 will be acts of omission.</p>
							</Card.Content>
						</Card.Root>
					</div>
				</div>
			</div>
		</div>

		<div class="relative">
			<div class="">
				<div class="flex">
					<div class="ml-[4%] xl:ml-[10.2%]">
						<ChevronUp class="h-8 w-8 text-[#778FB1]" />
					</div>
				</div>
			</div>
		</div>

		<!-- Item #4 -->
		<div class="relative">
			<div class="mb-3 items-center md:flex md:space-x-4">
				<div class="-ml-24 xl:ml-0 flex items-center">
					<!-- Icon -->
					<div class="ml-2 flex h-6 w-6 items-end justify-center rounded-full md:order-1">
						<img src={Icon1} alt="icon" />
					</div>
					<div
						class="font-caveat -ml-4 flex w-full flex-col justify-end text-xs font-medium text-gray-500"
					>
						<Avatar.Root class="ml-24 flex justify-end ml-28 xl:ml-24 flex justify-end w-6 h-6 xl:h-10 xl:w-10">
							<Avatar.Image class="flex justify-end" src={BetterUp} alt="@shadcn" />
							<Avatar.Fallback>CN</Avatar.Fallback>
						</Avatar.Root>
						<p class="flex w-full justify-end text-lg font-bold text-black">BetterUp</p>
						<p>San Francisco Bay Area</p>
						<p class="flex justify-end">Joined</p>
						<p class="flex justify-end">Sep 2022</p>
					</div>
				</div>
				<div class="ml-44">
					<div class="ml-10 flex gap-5">
						<Card.Root class="w-[600px] xl:w-[710px] border-0 shadow-md">
							<Card.Header>
								<Card.Title>VP Engineering</Card.Title>
								<Card.Description>Full-time</Card.Description>
							</Card.Header>
						</Card.Root>
					</div>
				</div>
			</div>
		</div>

		<div class="relative">
			<div class="">
				<div class="flex">
					<div class="ml-[10%]">
						<ChevronUp class="h-2 w-2 text-white" />
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
