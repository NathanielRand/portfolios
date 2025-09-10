<script>
	import '../app.pcss';
  	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, Button, Input, Footer, FooterCopyright, FooterLinkGroup, FooterBrand, FooterLink } from 'flowbite-svelte';
	
	// Global colors
	let background_color = "[#c4c4c4]";
</script>

<Navbar class="bg-{background_color} fixed w-full z-20 top-0 start-0">
	<NavBrand href="/">
		<span class="text-neumorphism self-center whitespace-nowrap text-6xl xl:text-8xl font-black uppercase subpixel-antialiased">Rand</span>
	</NavBrand>
	<div class="flex md:order-2">
		<a href="/#contact" class="px-4 py-3 text-3xl xl:text-4xl tracking-wider font-black uppercase text-white bg-{background_color} hidden md:flex neumorphism">Contact</a>
		<NavHamburger class="text-black"/>
	</div>
	<NavUl class="order-1 uppercase">
		<Button href="/#contact" size="lg" class="mb-4 text-4xl text-black font-thin bg-{background_color} md:hidden uppercase">Contact</Button>
		<NavLi href="/#about" class="text-4xl md:text-3xl xl:text-5xl font-thin text-black/60 subpixel-antialiased">About</NavLi>
		<NavLi href="/#work" class="text-4xl md:text-3xl xl:text-5xl font-thin text-black/60 subpixel-antialiased">Work</NavLi>
		<NavLi href="/#testimonials" class="text-4xl md:text-3xl xl:text-5xl font-thin text-black/60 subpixel-antialiased">Testimonials</NavLi>
	</NavUl>
</Navbar>

<slot />

<Footer footerType="logo" class="bg-[#c4c4c4] rounded-none">
	<svg class="mx-auto" width="6em" height="6em" viewBox="0 0 76 76" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" baseProfile="full" enable-background="new 0 0 76.00 76.00" xml:space="preserve" transform="scale(-1, 1)">
        <path fill="#4e4e4e" fill-opacity="0.5" stroke-linejoin="round" d="M 44.5,18.5C 45.8807,18.5 47,20.2909 47,22.5C 47,24.7091 45.8807,26.5 44.5,26.5C 43.1193,26.5 42,24.7091 42,22.5C 42,20.2909 43.1193,18.5 44.5,18.5 Z M 39.25,19.75C 40.0784,19.75 40.75,20.8693 40.75,22.25C 40.75,23.6307 40.0784,24.75 39.25,24.75C 38.4216,24.75 37.75,23.6307 37.75,22.25C 37.75,20.8693 38.4216,19.75 39.25,19.75 Z M 35,21C 35.8284,21 36.5,21.8954 36.5,23C 36.5,24.1046 35.8284,25 35,25C 34.1716,25 33.5,24.1046 33.5,23C 33.5,21.8954 34.1716,21 35,21 Z M 31.5,23.25C 32.3284,23.25 33,24.1454 33,25.25C 33,26.3546 32.3284,27.25 31.5,27.25C 30.6716,27.25 30,26.3546 30,25.25C 30,24.1454 30.6716,23.25 31.5,23.25 Z M 28.75,26.75C 29.3023,26.75 29.75,27.4216 29.75,28.25C 29.75,29.0784 29.3023,29.75 28.75,29.75C 28.1977,29.75 27.75,29.0784 27.75,28.25C 27.75,27.4216 28.1977,26.75 28.75,26.75 Z M 34,27.5C 43,23 49.2428,31.3086 42,40C 37,46 51.1334,55.5428 42,57.5C 35,59 37.1925,49.8978 35,46C 26,30 34,27.5 34,27.5 Z "/>
    </svg>   
	<hr class="my-6 border-gray-300 sm:mx-auto lg:my-8" />
	<FooterCopyright href="/" by="Nathaniel Rand™" />
</Footer>

<style>
	:root {
    --colorMain: #d2d2d2;
    --brShadow: -6px 6px 15px rgba(0,0,0,0.5);
    --tlShadow: 6px -6px 15px rgba(255,255,255,0.8);
    }

	/* Neumorphism */
	.neumorphism {
		border-radius: 50px;
		background: #c4c4c4;
		box-shadow:  -6px 6px 12px #a7a7a7,
					6px -6px 12px #e1e1e1;
	}
	/* Neumorphism Inverted*/
	.invert-neumorphism {
		border-radius: 50px;
		background: #c4c4c4;
		box-shadow: inset -6px 6px 12px #a7a7a7,
					inset 6px -6px 12px #e1e1e1;
	}
	/* Hover:Neumorphism */
	.neumorphism:hover {
		border-radius: 50px;
		background: #c4c4c4;
		box-shadow: inset -6px 6px 12px #a7a7a7,
            inset 6px -6px 12px #e1e1e1;
	}
	/* Navbar - Neumorphism */
	.nav-neumorphism {
        background: #c4c4c4;
        box-shadow: -6px 6px 12px #a7a7a7,
                    6px -6px 12px #e1e1e1;
    }
	/* Text - Neumorphism */
	.text-neumorphism {
        color: var(--colorMain);
        letter-spacing: 0.03em;
        text-transform: uppercase;
        text-shadow: var(--brShadow), 
                    var(--tlShadow);
        position: relative;
    }
    .text-neumorphism::before,
    .text-neumorphism::after {
        position: absolute;
        background: var(--colorMain);
        content: '';
        border-radius: 10%;
    }
</style>
