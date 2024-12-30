<script setup>
	import logoNav from '@/assets/Images/logonav.png'
</script>
<template>
	<div class="navbar container mx-auto">
		<div class="navbar-start">

			<div class="flex items-center space-x-4">
				<img :src="logoNav" />
				<p class="text-xl text-text font-semibold">Undisan Eco Village</p>
			</div>
		</div>
		<div class="navbar-center">

		</div>
		<div class="navbar-end">
			<div class="dropdown dropdown-end">
				<div tabindex="0" role="button" class="btn btn-ghost lg:hidden">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						class="h-5 w-5"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor">
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M4 6h16M4 12h8m-8 6h16" />
					</svg>
				</div>
				<div
					tabindex="0"
					class="menu menu-sm dropdown-content bg-base-100 rounded-box z-[1] mt-3 w-52 p-2 shadow space-y-4">
					<a href="">Item 1</a>
					<a href="">Item 2</a>
					<a href="">Item 3</a>
					<a href="">Item 4</a>
				</div>
			</div>
			<div class=" space-x-4 hidden lg:flex">
				<a href="">Item 1</a>
				<a href="">Item 2</a>
				<a href="">Item 3</a>
				<a href="">Item 4</a>
			</div>
		</div>
	</div>
</template>
