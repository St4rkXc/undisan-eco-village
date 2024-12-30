<script setup>
import landingHero from '@/components/Landing/LandingHero.vue'
import Navbar from '@/components/Landing/Navbar.vue'
import LandingFunfact from '@/components/Landing/LandingFunfact.vue'
import dayaTarik from '@/components/Landing/LandingTarik.vue'
import landingHotel from '@/components/Landing/landingHotel.vue';
import LandingCTA from '@/components/Landing/LandingCTA.vue';

</script>

<template>
	<Navbar />
	<landingHero />
	<div class="bg-white">
		<landingFunfact />
		<dayaTarik />
		<landingHotel	/>
	</div>
	<LandingCTA />
</template>
