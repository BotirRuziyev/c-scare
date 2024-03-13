<template>
  <footer class="footer">
    <div class="main_container">
      <div class="footer_menu">
        <div class="menu_card">
          <div class="head">Products</div>
          <nuxt-link to="#" class="nav_link">User scoring</nuxt-link>
          <nuxt-link to="#" class="nav_link">Group scoring</nuxt-link>
          <nuxt-link to="#" class="nav_link">Transaction monitoring</nuxt-link>
          <nuxt-link to="#" class="nav_link"
            >Traffic profitability forecast</nuxt-link
          >
        </div>
        <div class="menu_card">
          <div class="head">Industries</div>
          <nuxt-link to="#" class="nav_link">I-GAMING</nuxt-link>
          <nuxt-link to="#" class="nav_link">Fintech</nuxt-link>
          <nuxt-link to="#" class="nav_link">Crypto</nuxt-link>
          <nuxt-link to="#" class="nav_link">Trading</nuxt-link>
        </div>
        <div class="menu_card">
          <div class="head">Guidelines</div>
          <nuxt-link to="#" class="nav_link">Guides & Reports</nuxt-link>
          <nuxt-link to="#" class="nav_link">Success stories</nuxt-link>
          <nuxt-link to="#" class="nav_link">Blog</nuxt-link>
        </div>
        <div class="menu_card">
          <div class="head">C-SCORE</div>
          <nuxt-link to="#" class="nav_link">News</nuxt-link>
          <nuxt-link to="#" class="nav_link">Partners</nuxt-link>
          <nuxt-link to="#" class="nav_link">Careers</nuxt-link>
          <nuxt-link to="#" class="nav_link">Security and Compliance</nuxt-link>
          <nuxt-link to="#" class="nav_link">API’s</nuxt-link>
          <nuxt-link to="#" class="nav_link">Contacts</nuxt-link>
          <nuxt-link to="#" class="nav_link">Pricing</nuxt-link>
        </div>
      </div>
      <div class="messengers">
        <div class="left_block">
          For media partners: <nuxt-link to="#">pr@c-score.io</nuxt-link>
        </div>
        <div class="right_block">
          <a href="#">
            <img src="~/assets/img/icons/youtube.svg" alt="" />
          </a>
          <a href="#">
            <img src="~/assets/img/icons/in.svg" alt="" />
          </a>
          <a href="#">
            <img src="~/assets/img/icons/fb.svg" alt="" />
          </a>
          <a href="#">
            <img src="~/assets/img/icons/tg.svg" alt="" />
          </a>
          <a href="#">
            <img src="~/assets/img/icons/tw.svg" alt="" />
          </a>
        </div>
      </div>
      <div class="footer_bottom">
        <div class="logo">
          <nuxt-link to="/">
            <img src="~/assets/img/logo.svg" alt="" />
          </nuxt-link>
        </div>
        <div class="copyright">
          © C-SCORE tm (Thai), 2023. All rights reserved.
        </div>
        <div class="right_block">
          <nuxt-link to="#">Privacy Notice</nuxt-link>
          <nuxt-link to="#">Cookie Policy</nuxt-link>
          <nuxt-link to="#">Terms Of Use</nuxt-link>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
.footer {
  background: rgb(1, 14, 38);
  padding: 48px 0 30px;
  .footer_menu {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 20px;
    .menu_card {
      .head {
        color: rgb(255, 255, 255);
        font-size: 16px;
        font-weight: 400;
        line-height: 19.2px;
        letter-spacing: 0%;
        text-align: left;
        margin-bottom: 11px;
      }
      .nav_link {
        display: block;
        color: rgb(163, 163, 197);
        font-size: 14px;
        font-weight: 400;
        line-height: 19.6px;
        letter-spacing: 0%;
        text-align: left;
        margin-bottom: 13px;
        transition: 0.3s;
        &:hover {
          color: rgb(255, 255, 255);
        }
      }
    }
  }
  .messengers {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 21px 0;
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
    border-top: 1px solid rgba(255, 255, 255, 0.1);
    .left_block {
      font-size: 16px;
      font-weight: 400;
      line-height: 19.2px;
      letter-spacing: 0%;
      text-align: left;
      color: rgb(255, 255, 255);
      a {
        color: rgb(64, 87, 217);
      }
    }
    .right_block {
      display: flex;
      gap: 10px;
      img {
        border-radius: 100%;
        transition: 0.3s;
        &:hover {
          background: rgba(255, 255, 255, 0.05);
          transform: scale(1.1);
        }
      }
    }
  }
  .footer_bottom {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-top: 20px;
    .copyright {
      color: rgb(163, 163, 197);
      font-size: 14px;
      font-weight: 400;
      line-height: 25.2px;
      letter-spacing: 0%;
      text-align: left;
    }
    .right_block {
      display: flex;
      align-items: center;
      gap: 20px;
      a {
        color: rgb(163, 163, 197);
        font-family: Poppins;
        font-size: 14px;
        font-weight: 400;
        line-height: 25.2px;
        letter-spacing: 0%;
        text-align: left;
        text-decoration-line: underline;
      }
    }
  }
}
@media (max-width: 992px) {
  .footer {
    .footer_menu {
      grid-template-columns: repeat(2, 1fr);
    }
    .footer_bottom {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      column-gap: 20px;
      .copyright {
        grid-column: 2/4;
      }
      .right_block {
        grid-column: 1/4;
        justify-content: space-between;
        margin-top: 20px;
      }
    }
  }
}
@media (max-width: 576px) {
  .footer {
    .footer_menu {
      grid-template-columns: repeat(1, 1fr);
      .menu_card {
        .head {
          font-size: 14px;
        }
        .nav_link {
          font-size: 12px;
        }
      }
    }
    .messengers {
      padding: 15px 0;
      flex-direction: column;
      .left_block {
        margin-bottom: 10px;
        font-size: 14px;
      }
      .right_block {
        gap: 15px;
      }
      img {
        height: 35px;
      }
    }
    .footer_bottom {
      grid-template-columns: repeat(1, 1fr);
      .logo {
        img {
          height: 50px;
        }
      }
      .copyright {
        font-size: 12px;
        grid-column: auto;
      }
      .right_block {
        grid-column: auto;
        margin-top: 15px;
        a {
          font-size: 12px;
        }
      }
    }
  }
}
</style>
