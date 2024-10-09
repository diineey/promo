<script setup>
import BaseButton from '@/shared/UI/BaseButton.vue'
import LanguagesSwitch from '@/shared/composables/languages-switch/LanguagesSwitch.vue'
</script>

<template>
  <header class="header-wrapper">
    <div class="header-section-black">
      <img src="@/assets/img/logo.svg" alt="logo">

      <div class="header-section-text">
        <h1 v-html="$t('header-title')"/>

        <p v-html="$t('header-text')" class="header-section-p" />

        <BaseButton color="--white"/>
      </div>
    </div>

    <div class="header-section-blue">
      <div class="lang">
        <LanguagesSwitch />
      </div>

      <div class="header-img">
        <img class="header-img" src="@/assets/img/header-img.svg" alt="" />
      </div>
    </div>
  </header>
</template>

<style>
.header-wrapper {
  display: flex;
  width: 100%;
  height: 100%;
  background-color: var(--blue);
  border-radius: 0 0 30px 30px;
}

.header-section-black {
  background-color: var(--black);
  width: 50%;
  padding: 33px 0 0 60px;
  color: var(--white);
  border-radius: 0 0 0 30px;
}

.header-section-blue {
  background-color: var(--blue);
  width: 50%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 30px 0 0 0;
  border-radius: 0 0 30px 0;
}

.header-section-blue:nth-child(1) {
  display: flex;
  align-items: center;
  justify-content: center;
}

.header-section-text {
  padding: 136px 52px 105px 0;
}

.header-section-p {
  font-size: 20px;
  font-weight: 500;
  line-height: 26px;
  padding: 41px 0 24px 0;
}

.lang {
  display: flex;
  height: 24px;
  justify-content: end;
  padding-right: 60px;
}

.header-img {
  display: flex;
  justify-content: center;
  align-items: center;
}

.header-img img {
  width: 602px;
  height: auto;
}

@media screen and (max-width: 1300px) {
  .header-img img {
    width: 500px;
    height: auto;
    padding-top: 136px;
  }
}

@media screen and (max-width: 1023px) {
  .header-wrapper {
    flex-direction: column;
    border-radius: 0 0 26px 26px;
  }

  .header-section-black,
  .header-section-blue {
    width: 100%;
    border-radius: 0 0 26px 26px;
  }

  .header-section-blue {
    padding: 0;
  }

  .header-img img {
    padding: 0;
  }

  .lang {
    display: none;
    padding: 0;
  }
}

@media screen and (max-width: 768px) {
  br {
    display: none;
  }

  .header-section-black {
    padding: 40px 20px 30px 20px;
  }

  .header-section-black img {
    width: 134px;
  }

  .header-section-text {
    padding: 45px 0 10px 0;
  }

  .header-section-p {
    font-size: 18px;
    line-height: 23px;
    padding: 16px 0 20px 0;
  }

  .header-section-blue {
    padding: 0;
  }

  .header-img img {
    padding: 0;
    width: 400px;
    height: auto;
  }
}

@media screen and (max-width: 425px) {
  .header-img img {
    width: 339px;
    height: auto;
  }
}

@media screen and (max-width: 350px) {
  .header-img img {
    width: 300px;
    height: auto;
  }
}
</style>
