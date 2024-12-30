<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Scrollbar, Autoplay } from 'swiper/modules' // Import Scrollbar here
import 'swiper/css'
import 'swiper/css/scrollbar' // Import Swiper Scrollbar CSS
import 'swiper/css/autoplay'

import Dkarang from '@/assets/Images/Hotel/Dkarang.jpg'
import Dklumpu from '@/assets/Images/Hotel/Dklumpu.jpg'
import Dsari from '@/assets/Images/Hotel/Dsari.jpg'
import Dumah from '@/assets/Images/Hotel/Dumah.jpg'
import Karang from '@/assets/Images/Hotel/Karang.jpeg'
import Manda from '@/assets/Images/Hotel/Manda.jpg'
import Rindu from '@/assets/Images/Hotel/Rindu.webp'
import Saren from '@/assets/Images/Hotel/Saren.jpg'

// ! Autoplay harus di import & Moduleskan

// Swiper options defined in a single object
const swiperOptions = {
	modules: [Scrollbar, Autoplay], // Add modules to swiper options
	loop: true,
	spaceBetween: 20,
	autoplay: {
		delay: 2000,
		disableOnInteraction: false,
	},
	pagination: {
		clickable: true,
		dynamicBullets: true,
	},
	navigation: {
		nextEl: '.swiper-button-next',
		prevEl: '.swiper-button-prev',
	},
	scrollbar: {
		draggable: true,
		el: '.swiper-scrollbar',
	},
	breakpoints: {
		640: {
			slidesPerView: 2,
		},
		768: {
			slidesPerView: 2,
		},
		1200: {
			slidesPerView: 3,
		},
		1400: {
			slidesPerView: 4,
		},
	},
}

// Methods for handling Swiper events
const onSwiper = (swiper) => {
	console.log('Swiper initialized:', swiper)
}

const onSlideChange = () => {
	console.log('Slide change')
}
</script>

<template>
	<section class="py-[100px] container mx-auto px-3" id="hotel">
		<!-- Bind swiperOptions using v-bind -->
		<div class="flex flex-col items-center justify-center mx-auto text-center max-w-[800px]">
			<div class="my-badge">undisan</div>
			<h2 class="section-title">
				Stay & Enjoy <br />
				Undisan Eco Village
			</h2>
			<p class="text-text/80 text-center mt-4">
				Undisan Eco Village menawarkan pengalaman yang tenang dan mendalam di alam, memungkinkan pengunjung untuk bersantai dan terhubung kembali dengan lingkungan. Tempat
				ini menjadi destinasi sempurna bagi mereka yang mencari kedamaian dan petualangan yang selaras dengan alam.
			</p>
		</div>
		<div class="mt-16">
			<swiper v-bind="swiperOptions" @swiper="onSwiper" @slideChange="onSlideChange" class="pb-9">
				<!-- Biar scrollbarnya agak kebawh -->
				<swiper-slide>
					<img :src="Dklumpu" alt="" class="w-full h-[300px] object-cover rounded-3xl" />
					<div class="mt-4 -space-y-1">
						<p class="text-text text-xl font-semibold">De Klumpu Bali Eco Tradi Stay</p>
						<p class="text-text/80 text-lg font-semibold">Rp1.950.000</p>
					</div>
				</swiper-slide>
				<swiper-slide>
					<img :src="Dsari" alt="" class="w-full h-[300px] object-cover rounded-3xl" />
					<div class="mt-4 -space-y-1">
						<p class="text-text text-xl font-semibold">D’Sari Undisan House</p>
						<p class="text-text/80 text-lg font-semibold">Rp158.000</p>
					</div>
				</swiper-slide>
				<swiper-slide>
					<img :src="Dumah" alt="" class="w-full h-[300px] object-cover rounded-3xl" />
					<div class="mt-4 -space-y-1">
						<p class="text-text text-xl font-semibold">De Umah Bali Eco tradi Home</p>
						<p class="text-text/80 text-lg font-semibold">Rp540.000</p>
					</div>
				</swiper-slide>
				<swiper-slide>
					<img :src="Dkarang" alt="" class="w-full h-[300px] object-cover rounded-3xl" />
					<div class="mt-4 -space-y-1">
						<p class="text-text text-xl font-semibold">D’Karang Eco Lodge</p>
						<p class="text-text/80 text-lg font-semibold">Rp300.000</p>
					</div>
				</swiper-slide>
				<swiper-slide>
					<img :src="Manda" alt="" class="w-full h-[300px] object-cover rounded-3xl" />
					<div class="mt-4 -space-y-1">
						<p class="text-text text-xl font-semibold">Pondok Manda</p>
						<p class="text-text/80 text-lg font-semibold">Rp321.644</p>
					</div>
				</swiper-slide>
				<swiper-slide>
					<img :src="Saren" alt="" class="w-full h-[300px] object-cover rounded-3xl" />
					<div class="mt-4 -space-y-1">
						<p class="text-text text-xl font-semibold">Umah Saren Homestay</p>
						<p class="text-text/80 text-lg font-semibold">Rp625.418</p>
					</div>
				</swiper-slide>
				<swiper-slide>
					<img :src="Rindu" alt="" class="w-full h-[300px] object-cover rounded-3xl" />
					<div class="mt-4 -space-y-1">
						<p class="text-text text-xl font-semibold">Rindu Homestay</p>
						<p class="text-text/80 text-lg font-semibold">Rp272.726</p>
					</div>
				</swiper-slide>
				<swiper-slide>
					<img :src="Karang" alt="" class="w-full h-[300px] object-cover rounded-3xl" />
					<div class="mt-4 -space-y-1">
						<p class="text-text text-xl font-semibold">Puri Karang Undisan</p>
						<p class="text-text/80 text-lg font-semibold">Rp455.000</p>
					</div>
				</swiper-slide>
				<div class="swiper-scrollbar mt-32 "></div>
			</swiper>
		</div>
	</section>
</template>
