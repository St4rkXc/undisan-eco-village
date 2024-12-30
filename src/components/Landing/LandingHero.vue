<script setup>
import HeroImage from '@/assets/Images/Hero.png'
</script>

<template>
	<header class="container mx-auto pt-[50px] pb-[100px] px-3">
		<div class="flex flex-col 2xl:flex-row 2xl:justify-between 2xl:items-center gap-y-4 gap-x-24">
			<div class="max-w-[800px] flex flex-col gap-y-2 md:gap-y-0">
				<div class="my-badge w-fit">
					undisan
				</div>
				<h1 class="section-title max-w-[800px]">
					Desa Undisan Salah Satu Desa Wisata Terbaik Di Bali
				</h1>
			</div>
			<p class="text-text/80  max-w-[700px]">Terletak di Kecamatan Tembuku, Kabupaten Bangli, Provinsi Bali, Desa Undisan adalah salah satu desa wisata terbaik di Bali. Desa ini menawarkan keindahan alam yang asri, tradisi budaya yang kental, dan keramahan khas masyarakat lokal, menjadikannya destinasi ideal untuk menikmati kehidupan Bali yang autentik.</p>
		</div>
		<div class="mt-8 md:mt-16">
			<img :src="HeroImage" alt="Pemandangan Undisan" class="w-full h-[300px] md:h-[500px] object-cover rounded-3xl" />
		</div>
	</header>
</template>


