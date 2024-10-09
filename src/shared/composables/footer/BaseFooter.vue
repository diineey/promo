<template>
  <footer class="footer-wrapper">
    <div class="footer-content">
      <img class="footer-logo" src="@/assets/img/logo.svg" alt="logo">

      <div class="footer-icons">
        <a href="#">
          <img src="@/components/icons/linkedin.svg" alt="LinkedIn">
        </a>
        <a href="#">
          <img src="@/components/icons/telegram.svg" alt="Telegram">
        </a>
        <a href="#">
          <img src="@/components/icons/instagram.svg" alt="Instagram">
        </a>
      </div>
    </div>

    <hr class="footer-divider">

    <div class="footer-rights">
      © 2024 Mentory. All Rights Reserved
    </div>
  </footer>
</template>

<style scoped>
.footer-wrapper {
  width: 100%;
  background-color: var(--blue);
  padding-bottom: 16px;
}

.footer-content {
  padding: 40px 60px;
  display: flex;
  justify-content: space-between;
  width: 86%;
}

.footer-divider {
  width: 100%;
  height: 2px;
  background-color: var(--white);
  border: none;
}

.footer-icons {
  display: flex;
  gap: 18px;
}

.footer-rights {
  display: flex;
  justify-content: center;
  align-items: center;
  font-weight: 500;
  color: var(--white);
  font-size: 18px;
  line-height: 26px;
  padding-top: 19px;
}

@media screen and (max-width: 1024px) {
  .footer-content {
    width: 100%;
  }
}

@media screen and (max-width: 768px) {
  .footer-wrapper {
    padding: 0;
  }

  .footer-content {
    padding: 20px 20px 30px 20px;
    flex-direction: column;
    gap: 30px;
  }

  .footer-logo {
    width: 134px;
  }

  .footer-rights {
    font-size: 12px;
    line-height: 17px;
    justify-content: left;
    padding: 12px 20px;
  }

  .footer-icons {
    gap: 24px;
  }
}
</style>
