<script setup>
import useIsMobile from '@/shared/utils/useIsMobile.js'

const { isMobile } = useIsMobile()

const whyCards = [
  {
    imgSrc: new URL('../assets/img/personal.png', import.meta.url).href,
    altText: 'Personal Approach',
    title: 'personal-approach',
    description: 'personal-specialists'
  },
  {
    imgSrc: new URL('../assets/img/data-cloud.png', import.meta.url).href,
    altText: 'Feedback',
    title: 'feedback',
    description: 'feedback-help'
  },
  {
    imgSrc: new URL('../assets/img/rent.png', import.meta.url).href,
    altText: 'Easy booking',
    title: 'easy-booking',
    description: 'easy-booking-text'
  }
]
</script>

<template>
  <main class="why-wrapper">
    <div class="why-content">
      <div class="why-text">
        <h2 class="h2">
          {{ $t('why-we') }}
        </h2>

        <p v-html="$t('we-create')" class="text-center" />
      </div>

      <swiper-container
          v-if="isMobile"
          class="why-cards"
          :slides-per-view="1.1"
          :breakpoints="{
          '650': {
            slidesPerView: 2.5,
            spaceBetween: 20
          },
          '570': {
            slidesPerView: 2.2,
            spaceBetween: 20
          },
          '450': {
            slidesPerView: 1.8,
            spaceBetween: 20
         },
         '375': {
            slidesPerView: 1.4,
            spaceBetween: 20
         }
        }"
      >
        <swiper-slide v-for="(card, index) in whyCards" :key="'first-'+ index">
          <div class="why-card">
            <img :src="card.imgSrc" :alt="card.altText">
            <h3>{{ $t(card.title) }}</h3>
            <p class="text-center">{{ $t(card.description) }}</p>
          </div>
        </swiper-slide>
      </swiper-container>

      <div class="why-cards" v-else>
        <div class="why-card" v-for="(card, index) in whyCards" :key="'first-'+ index">
          <img :src="card.imgSrc" :alt="card.altText">
          <h3>{{ $t(card.title) }}</h3>
          <p class="text-center">{{ $t(card.description) }}</p>
        </div>
      </div>

    </div>
  </main>
</template>

<style scoped>
.why-wrapper {
  width: 100%;
  display: flex;
  justify-content: center;
}

.why-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 24px;
}

.why-text {
  max-width: 100%;
  width: 516px;
  display: flex;
  flex-direction: column;
  gap: 24px;
}

.why-cards {
  margin-top: 16px;
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
  justify-content: center;
}

.why-card {
  padding: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 314px;
  gap: 10px;
}

.why-cards img {
  width: 220px;
  height: 220px;
}

@media screen and (max-width: 768px) {
  .why-wrapper {
    padding-bottom: 40px;
  }

  .why-content {
    width: 100%;
    padding-top: 20px;
  }

  .why-cards {
    width: 100%;
  }

  .why-card {
    width: 240px;
    padding: 0;
    align-items: flex-start;
  }

  .why-card p, h3 {
    text-align: left;
  }

  .why-card img {
    width: 160px;
    height: 160px;
  }
}
</style>