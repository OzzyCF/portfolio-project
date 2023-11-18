<script>
	import {
		Navbar,
		NavBrand,
		NavLi,
		NavUl,
		NavHamburger,
		ImagePlaceholder,
		Skeleton,
		TextPlaceholder,
		Video
	} from 'flowbite-svelte';
</script>

<div class="relative px-8">
	<Navbar
		class="px-2 sm:px-4 py-2.5 fixed w-full z-20 top-0 left-0 border-b .mb-4 to-gray-400 shadow"
	>
		<NavBrand href="/">
			<img src="/Ozzy-frontEndDev-Logo.png" class="mr-3 h-6 sm:h-9" alt="Ozzy logo" />
			<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"
				>Oswaldo Colon Freites</span
			>
		</NavBrand>
		<NavHamburger />
		<NavUl>
			<NavLi href="/" active={true}>Home</NavLi>
			<NavLi href="/about">About</NavLi>

			<NavLi href="/projects">Projects</NavLi>
			<NavLi href="/contact">Contact</NavLi>
		</NavUl>
	</Navbar>
</div>
