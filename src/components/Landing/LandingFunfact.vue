<script setup>
import { ref } from 'vue'
import ProfesiImg from '@/assets/Images/Profesi.png'
import PariwisataImg from '@/assets/Images/Pariwisata.png'
import penghargaanImg from '@/assets/Images/Penghargaab.png'

const activeTab = ref('content1')

function tabs(tabName) {
	activeTab.value = tabName
}
</script>

<template>
	<section class="container mx-auto py-[100px]" id="company">
		<div class="flex flex-col items-center justify-center mx-auto">
			<div class="my-badge">undisan</div>
			<h2 class="section-title">Funfact Desa Undisan</h2>
		</div>
		<div class="flex flex-ol lg:flex-row mt-16">
			<!-- Bind active classes dynamically -->
			<p
				:class="[
					'flex-1 py-6 text-lg font-semibold text-center border-b-2 cursor-pointer text-text',
					activeTab === 'content1' ? 'border-b-primary' : 'border-b-primary/30',
				]"
				@click="tabs('content1')"
			>
				Profesi Masyarakat
			</p>
			<p
				:class="[
					'flex-1 py-6 text-lg font-semibold text-center border-b-2 cursor-pointer text-text',
					activeTab === 'content2' ? 'border-b-primary' : 'border-b-primary/30',
				]"
				@click="tabs('content2')"
			>
				Pariwisata
			</p>
			<p
				:class="[
					'flex-1 py-6 text-lg font-semibold text-center border-b-2 cursor-pointer text-text',
					activeTab === 'content3' ? 'border-b-primary' : 'border-b-primary/30',
				]"
				@click="tabs('content3')"
			>
				Penghargaan
			</p>
		</div>
		<div class="mt-16">
			<!-- Conditional rendering for each tab -->
			<div v-show="activeTab === 'content1'">
				<div class="flex flex-col lg:flex-row gap-8">
					<img :src="ProfesiImg" alt="" />
					<div class="space-y-4">
						<h3 class="text-2xl font-semibold text-text">Profesi Masyarakat</h3>
						<p class="text-base text-text/80">
							Sebagian besar masyarakat Desa Undisan menjalani kehidupan sebagai petani yang mengelola lahan pertanian mereka dengan tekun, peternak yang merawat
							berbagai jenis hewan ternak untuk memenuhi kebutuhan sehari-hari, serta pengrajin bunga sepuh emas, sebuah kerajinan tangan yang unik dan khas, di mana
							bahan dasar yang digunakan adalah kuningan, yang kemudian diproses dengan cermat dan penuh keahlian untuk menciptakan karya seni bernilai tinggi.
						</p>
					</div>
				</div>
			</div>
			<div v-show="activeTab === 'content2'">
				<div class="flex flex-col lg:flex-row gap-8">
					<img :src="PariwisataImg" alt="" />
					<div class="space-y-4">
						<h3 class="text-2xl font-semibold text-text">Daya Tarik Wisata</h3>
						<p class="text-base text-text/80">
							Pada tahun 1990-an, masyarakat Desa Undisan mulai mengenal dan berinteraksi dengan dunia pariwisata, sebuah perubahan besar yang dipicu oleh beberapa
							tokoh lokal yang memiliki usaha di bidang travel, hotel, dan homestay. Kehadiran para pelaku usaha ini membuka peluang baru bagi masyarakat untuk
							terlibat dalam berbagai aktivitas yang mendukung sektor pariwisata, seperti menyediakan akomodasi, menjadi pemandu wisata, hingga memperkenalkan budaya
							lokal kepada wisatawan.
						</p>
					</div>
				</div>
			</div>
			<div v-show="activeTab === 'content3'">
				<div class="flex flex-col lg:flex-row gap-8">
					<img :src="penghargaanImg" alt="" />
					<div class="space-y-4">
						<h3 class="text-2xl font-semibold text-text">Penghargaan</h3>
						<p class="text-base text-text/80">
							Desa Undisan mencatat prestasi membanggakan dengan masuk dalam 50 besar desa wisata terbaik pada Anugerah Desa Wisata Indonesia (ADWI) 2022. Pencapaian
							ini merupakan hasil dari upaya masyarakat dan pemerintah setempat sejak ditetapkannya desa ini sebagai desa wisata melalui Surat Keputusan (SK) pada
							tahun 2014, menjadi tonggak penting dalam memperkuat identitasnya sebagai destinasi wisata unggulan di Indonesia.
						</p>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>
