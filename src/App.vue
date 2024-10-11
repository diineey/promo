<script setup>
import Header from '@/shared/composables/header/BaseHeader.vue'
import HowItWorks from '@/components/HowItWorks.vue'
import WhenToSearch from '@/components/WhenToSearch.vue'
import WhyWe from '@/components/WhyWe.vue'
import TelegramCard from '@/components/TelegramCard.vue'
import MainSteps from '@/components/MainSteps.vue'
import Footer from '@/shared/composables/footer/BaseFooter.vue'

import 'swiper/css';
import { register } from 'swiper/element/bundle'

register()
</script>

<template>

  <Header />

  <HowItWorks />

  <WhenToSearch />

  <MainSteps />

  <WhyWe />

  <TelegramCard />

  <Footer />

</template>
