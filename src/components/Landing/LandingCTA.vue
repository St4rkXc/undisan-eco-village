<script setup></script>
<template>
	<footer class="container py-[100px] mx-auto px-3">
		<div class="w-full h-[500px] footercta rounded-3xl relative flex justify-center items-center">
			<div class="absolute top-0 left-0 bg-black/30 w-full h-full rounded-3xl z-40"></div>
			<p class="section-title text-center text-white relative z-50">
				Book a Tour, <br />
				Enjoy Undisan Eco Village
			</p>
		</div>
		<div class="mt-12 flex flex-col sm:flex-row justify-between flex-wrap gap-8">
			<div class="flex-1">
				<p class="text-xl text-text font-semibold">Phone</p>
				<p class="text-lg text-text/80 font-medium">+62 813 3776 0265 (Bagus Indra)</p>
			</div>
			<div class="flex-1">
				<p class="text-xl text-text font-semibold">Email</p>
				<p class="text-lg text-text/80 font-medium">bagusastika009@gmail.com</p>
			</div>
			<div class="flex-1">
				<p class="text-xl text-text font-semibold">Social</p>
				<div class="flex gap-3">
					<a href="http://wa.me/+6281337760265" target="_blank" class="pi pi-whatsapp text-xl"></a>
					<a href="mailto:bagusastika009@gmail.com" target="" class="pi pi-envelope text-xl"></a>
				</div>
			</div>
		</div>
	</footer>
</template>
<style scoped>
.footercta {
	background-image: url(../../assets/Images/Hero.png);
	background-size: cover;
	background-position: center;
	background-repeat: no-repeat;
}
</style>
