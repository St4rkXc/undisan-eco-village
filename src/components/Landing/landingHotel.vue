<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Scrollbar, Autoplay } from 'swiper/modules'
import 'swiper/css'
import 'swiper/css/scrollbar'
import 'swiper/css/autoplay'

import HotelCard from '@/components/landingcompo/HomeStay.vue' // Import the reusable component

import Dkarang from '@/assets/Images/Hotel/Dkarang.jpg'
import Dklumpu from '@/assets/Images/Hotel/Dklumpu.jpg'
import Dsari from '@/assets/Images/Hotel/Dsari.jpg'
import Dumah from '@/assets/Images/Hotel/Dumah.jpg'
import Karang from '@/assets/Images/Hotel/Karang.jpeg'
import Manda from '@/assets/Images/Hotel/Manda.jpg'
import Rindu from '@/assets/Images/Hotel/Rindu.webp'
import Saren from '@/assets/Images/Hotel/Saren.jpg'

// Swiper options defined in a single object
const swiperOptions = {
	modules: [Scrollbar, Autoplay],
	loop: true,
	spaceBetween: 20,
	autoplay: {
		delay: 2000,
		disableOnInteraction: false,
	},
	scrollbar: {
		draggable: true,
		el: '.swiper-scrollbar',
	},
	breakpoints: {
		640: { slidesPerView: 2 },
		768: { slidesPerView: 2 },
		1200: { slidesPerView: 3 },
		1400: { slidesPerView: 4 },
	},
}

// Data for the slides
const hotels = [
	{ img: Dklumpu, title: 'De Klumpu Bali Eco Tradi Stay', price: 'Rp1.950.000' },
	{ img: Dsari, title: 'D’Sari Undisan House', price: 'Rp158.000' },
	{ img: Dumah, title: 'De Umah Bali Eco tradi Home', price: 'Rp540.000' },
	{ img: Dkarang, title: 'D’Karang Eco Lodge', price: 'Rp300.000' },
	{ img: Manda, title: 'Pondok Manda', price: 'Rp321.644' },
	{ img: Saren, title: 'Umah Saren Homestay', price: 'Rp625.418' },
	{ img: Rindu, title: 'Rindu Homestay', price: 'Rp272.726' },
	{ img: Karang, title: 'Puri Karang Undisan', price: 'Rp455.000' },
]
</script>

<template>
	<section class="py-[100px] container mx-auto px-3" id="hotel">
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
			<swiper v-bind="swiperOptions" class="pb-9">
				<!-- Dynamically render HotelCard components -->
				<swiper-slide v-for="(hotel, index) in hotels" :key="index">
					<HotelCard :img="hotel.img" :title="hotel.title" :price="hotel.price" />
					<!-- <img :src="hotel.img" alt="" class="w-full h-[300px] object-cover rounded-3xl" />
					<div class="mt-4 -space-y-1">
						<p class="text-text text-xl font-semibold">{{ hotel.title }}</p>
						<p class="text-text/80 text-lg font-semibold">{{ hotel.price }}</p>
					</div> -->
					<!-- <HotelCard v-for="(hotel, index) in hotels" :key="index" :img="hotel.img" :title="hotel.title" :price="hotel.price" /> -->
				</swiper-slide>
				<div class="swiper-scrollbar mt-32"></div>
			</swiper>
		</div>
	</section>
</template>
