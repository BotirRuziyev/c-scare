<template>
  <header class="header">
    <div class="main_container">
      <div class="header_in d-flex align-center justify-space-between">
        <div class="logo">
          <a href="#">
            <img src="~/assets/img/logo.svg" alt="logo" />
          </a>
        </div>
        <div
          class="header_menu d-md-flex d-none align-center justify-space-between"
        >
          <a href="#">Products</a>
          <a href="#">Solutions</a>
          <a href="#">Resources</a>
          <a href="#">About us</a>
          <a href="#">Pricing</a>
        </div>
        <div class="header_auth d-md-flex d-none">
          <nuxt-link to="#" class="sign_in">Sign in</nuxt-link>
          <nuxt-link to="#" class="sign_up">Start free</nuxt-link>
        </div>
        <button class="burger_menu d-md-none d-block">
          <img height="50" src="~/assets/img/burger.png" alt="" />
        </button>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
.header {
  width: 100%;
  position: absolute;
  top: 0;
  left: 0;
  z-index: 2;
  .header_in {
    gap: 30px;
    padding: 15px 0;
    .header_menu {
      max-width: 550px;
      width: 100%;
      a {
        color: rgb(163, 163, 197);
        font-size: 15px;
        font-weight: 500;
        line-height: 23px;
        letter-spacing: 0%;
        text-align: left;
        transition: 0.3s;
        &:hover {
          color: rgb(255, 255, 255);
        }
      }
    }
    .header_auth {
      gap: 10px;
      .sign_in {
        border: 1px solid rgba(106, 106, 165, 0.6);
        border-radius: 5px;
        padding: 13px 28px;
        color: rgb(255, 255, 255);
        font-size: 12px;
        font-weight: 400;
        line-height: 18px;
        letter-spacing: 1px;
        text-align: center;
        white-space: nowrap;
        transition: 0.3s;
        &:hover {
          background: #f7931e;
          color: rgb(255, 255, 255);
          border-color: #f7931e;
        }
      }
      .sign_up {
        border: 1px solid rgb(247, 147, 30);
        border-radius: 5px;
        padding: 13px 28px;
        color: rgb(255, 255, 255);
        font-size: 12px;
        font-weight: 400;
        line-height: 18px;
        letter-spacing: 1px;
        text-align: center;
        white-space: nowrap;
        transition: 0.3s;
        &:hover {
          background: #f7931e;
        }
      }
    }
  }
}
@media (max-width: 960px) {
  .header {
    .header_in {
      .burger_menu {
        img {
          filter: brightness(0) saturate(100%) invert(85%) sepia(93%)
            saturate(39%) hue-rotate(225deg) brightness(108%) contrast(101%);
        }
      }
    }
  }
}
@media (max-width: 600px) {
  .header {
    .header_in {
      .logo {
        img {
          height: 45px;
        }
      }
      .burger_menu {
        img {
          height: 33px;
        }
      }
    }
  }
}
</style>
