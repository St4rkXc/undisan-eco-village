<script setup name="LandingNavbar">
import { ref, onMounted, onUnmounted } from 'vue'
import logoNav from '@/assets/Images/logonav.png'

const isVisible = ref(true)
let lastScrollY = window.scrollY

const handleScroll = () => {
	if (window.scrollY > lastScrollY) {
		isVisible.value = false
	} else {
		isVisible.value = true
	}
	lastScrollY = window.scrollY
}

onMounted(() => {
	window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
	window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
	<div :class="['bg-gray-100 sticky top-0 z-50 transition-transform duration-300 py-2 ', { '-translate-y-full': !isVisible }]">
		<div class="navbar container mx-auto">
			<div class="navbar-start">
				<div class="flex items-center space-x-4">
					<img :src="logoNav" />
					<p class="text-xl text-text font-semibold">Undisan <span class="hidden sm:inline">Eco Village</span></p>
				</div>
			</div>
			<div class="navbar-end">
				<div class="dropdown dropdown-end">
					<div tabindex="0" role="button" class="btn btn-ghost lg:hidden">
						<svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
							<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h8m-8 6h16" />
						</svg>
					</div>
					<div tabindex="0" class="menu menu-sm dropdown-content bg-base-100 rounded-box z-[1] mt-3 w-52 p-2 shadow space-y-1">
						<a href="#hero" class="navlink py-4">Undisan</a>
						<a href="#funfact" class="navlink py-4">FunFact</a>
						<a href="#pesona" class="navlink py-4">Pesona</a>
						<a href="#hotel" class="navlink py-4">Home Stay</a>
					</div>
				</div>
				<div class="space-x-4 hidden lg:flex">
					<a href="#hero" class="navlink">Undisan</a>
					<a href="#funfact" class="navlink">FunFact</a>
					<a href="#pesona" class="navlink">Pesona</a>
					<a href="#hotel" class="navlink">Home Stay</a>
				</div>
			</div>
		</div>
	</div>
</template>
