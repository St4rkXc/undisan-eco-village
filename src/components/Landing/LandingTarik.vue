<script setup>
import Ecovillgeimg from '@/assets/Images/Ecovillage.png'
import AirterjunImg from '@/assets/Images/Airterjun.jpg'
import PersawahanImg from '@/assets/Images/Persawahan.jpg'
import VanillaFarmImg from '@/assets/Images/vanillafarm.jpg'
import MemasakImg from '@/assets/Images/Memasak.jpg'
import KerajinanImg from '@/assets/Images/Kerajinan.jpg'
import MinyakImg from '@/assets/Images/MinyakKelapa.jpg'
</script>
<template>
	<section class="container mx-auto py-[100px] px-3" id="dayaTarik">
		<img :src="Ecovillgeimg" alt="" class="rounded-3xl w-full h-[600px] object-cover" />
		<div class="flex flex-col 2xl:flex-row 2xl:justify-between 2xl:items-center gap-y-8 gap-x-24 mt-16">
			<div class="max-w-[800px] flex flex-col">
				<div class="my-badge w-fit">undisan</div>
				<h1 class="section-title max-w-[800px]">Pesona & Daya Tarik Desa Undisan</h1>
			</div>
			<p class="text-text/80 max-w-[700px]">
				Desa Undisan menawarkan keindahan alam yang asri dengan sawah, kebun, dan perbukitan, serta kekayaan budaya lokal seperti kerajinan bunga sepuh emas dan upacara
				adat. Desa ini juga mengedepankan pariwisata berkelanjutan dan diakui sebagai salah satu desa wisata terbaik dalam Anugerah Desa Wisata Indonesia (ADWI) 2022.
			</p>
		</div>
		<div class="mt-16">
			<div class="pb-3 border-b-2 border-b-primary/40 w-full text-primary text-lg font-semibold">Daya Tarik Alam</div>
			<div class="grid grid-cols-1 lg:grid-cols-2 xl:grid-cols-3 gap-6 mt-6">
				<div class="">
					<img :src="AirterjunImg" alt="" class="w-full h-[400px] object-cover rounded-3xl" />
					<p class="text-text text-xl font-semibold p-2">Air Terjun Krisik</p>
				</div>
				<div class="">
					<img :src="PersawahanImg" alt="" class="w-full h-[400px] object-cover rounded-3xl" />
					<p class="text-text text-xl font-semibold p-2">Persawahan</p>
				</div>
				<div class="">
					<img :src="VanillaFarmImg" alt="" class="w-full h-[400px] object-cover rounded-3xl" />
					<p class="text-text text-xl font-semibold p-2">Organic Villa Farm</p>
				</div>
			</div>
			<div class="pb-3 border-b-2 border-b-primary/40 w-full text-primary text-lg font-semibold mt-12">Daya Tarik Lainnya</div>
			<div class="grid grid-cols-1 lg:grid-cols-2 xl:grid-cols-3 gap-6 mt-6">
				<div class="">
					<img :src="MinyakImg" alt="" class="w-full h-[400px] object-cover rounded-3xl" />
					<p class="text-text text-xl font-semibold p-2">Atraksi Membuat Minyak Kelapa</p>
				</div>
				<div class="">
					<img :src="KerajinanImg" alt="" class="w-full h-[400px] object-cover rounded-3xl" />
					<p class="text-text text-xl font-semibold p-2">Kerajinan</p>
				</div>
				<div class="">
					<img :src="MemasakImg" alt="" class="w-full h-[400px] object-cover rounded-3xl" />
					<p class="text-text text-xl font-semibold p-2">Atraksi Memasak</p>
				</div>
			</div>
		</div>
	</section>
</template>
