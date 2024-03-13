<template>
  <main class="index_page">
    <!-- // home start -->
    <section class="home">
      <div class="main_container">
        <h1 class="title"><span>Pricing</span> & Plans</h1>
        <p class="description">
          Select a plan that meets your needs. Get a perfect mix of high class
          fraud protection and user Social Rating
        </p>
        <div class="home_filter_btns">
          <button
            class="growing_btn"
            :class="filter ? 'active' : ''"
            @click="filter = true"
          >
            Growing
          </button>
          <button
            class="enterprise_btn"
            :class="!filter ? 'active' : ''"
            @click="filter = false"
          >
            Enterprise
          </button>
        </div>
        <div class="growing_container" :class="filter ? 'growing_active' : ''">
          <div class="growing_card" v-for="item of growing" :key="item.id">
            <div class="tariff">{{ item.tarif }}</div>
            <div class="growing_amount">
              <div class="valute_icon">€</div>
              <div class="right_block">
                <span class="growing_sum">{{ item.sum }}</span>
                {{ item.lifetime }}
              </div>
            </div>
            <div class="growing_list">
              <ul>
                <li class="list_item" v-for="(list, i) in item.list" :key="i">
                  <img src="~/assets/img/icons/list_icon.svg" alt="" />
                  <span>{{ list }}</span>
                </li>
              </ul>
            </div>
            <nuxt-link to="#" class="growing_link">
              <img src="~/assets/img/icons/link_icon.svg" alt="" />
            </nuxt-link>
          </div>
        </div>
        <div
          class="enterprise_container"
          :class="!filter ? 'enterprise_active' : ''"
        >
          <div class="enterprise_plan">
            <div class="card_left">
              <div class="head">From 60 000 API calls</div>
              <div class="title">Enterprise plan</div>
              <p class="description">
                Take advantage of everything C-SCORE’s platform can offer.
                Non-Doc verification, all-round anti-fraud, Social Rate &
                traffic profitability forecast; review your affiliate partners
                quickly; and customize your integration for better and optimized
                results
              </p>
              <button class="start_free_btn">Start free for 1 month</button>
            </div>
            <div class="card_list">
              <ul>
                <li class="list_item">
                  <img src="~/assets/img/icons/list_icon.svg" alt="" />
                  <span>Custom Api integration</span>
                </li>
                <li class="list_item">
                  <img src="~/assets/img/icons/list_icon.svg" alt="" />
                  <span
                    >Personal 24/7 customer manager and tech specialist</span
                  >
                </li>
                <li class="list_item">
                  <img src="~/assets/img/icons/list_icon.svg" alt="" />
                  <span>Private anti-fraud trainings and cases</span>
                </li>
                <li class="list_item">
                  <img src="~/assets/img/icons/list_icon.svg" alt="" />
                  <span>Unlimited Api calls</span>
                </li>
                <li class="list_item">
                  <img src="~/assets/img/icons/list_icon.svg" alt="" />
                  <span>10-100+ queries / sec</span>
                </li>
                <li class="list_item">
                  <img src="~/assets/img/icons/list_icon.svg" alt="" />
                  <span>Individual service optimization</span>
                </li>
              </ul>
              <button class="start_free_btn">Start free for 1 month</button>
            </div>
          </div>
          <div class="enterprise_cards">
            <div class="card_item" v-for="item of enterprise" :key="item.id">
              <div class="card_left">
                <div class="title">{{ item.title }}</div>
                <p class="description">
                  {{ item.description }}
                </p>
              </div>
              <div class="card_list">
                <ul>
                  <li class="list_item" v-for="(list, i) in item.list" :key="i">
                    <div class="circle"></div>
                    <div>{{ list }}</div>
                  </li>
                </ul>
              </div>
            </div>
            <div class="card_right"></div>
          </div>
        </div>
      </div>
    </section>
    <!-- // home end -->

    <!-- free access start -->
    <FreeAccess />
    <!-- free access end -->

    <!-- cards start -->
    <section class="cards">
      <div class="main_container">
        <div class="card_item">
          <div class="card_body">
            <h2 class="title">
              <span>Social Rate</span> & <br />
              Non-Doc verification
            </h2>
            <p class="description">
              C-SCORE creates a complete psychological profile of the user at an
              early stage, highlighting suspicious users and VIP players,
              allowing you to increase business profits with smart and accurate
              marketing campaigns
            </p>
          </div>
          <div class="right_block">
            <div class="about_user_container">
              <div class="about_user">
                <div class="name">Stephan Clarke </div>
                <div class="social_rate">Social Rate: <span>75%</span></div>
                <div class="safe"><span></span> safe</div>
                <div class="age list_item">
                  <img src="~/assets/img/icons/age.svg" alt="" /> Age: 28 y.o.
                </div>
                <div class="gender list_item">
                  <img src="~/assets/img/icons/gender.svg" alt="" />Gender: Male
                </div>
                <div class="country list_item">
                  <img src="~/assets/img/icons/country.svg" alt="" />Country:
                  Canada
                </div>
              </div>
            </div>
            <img class="card_img" src="~/assets/img/cards/1.png" alt="1" />
            <div class="interest">
              <div class="interest_top">
                <svg
                  width="13.000000"
                  height="14.000000"
                  viewBox="0 0 13 14"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                  xmlns:xlink="http://www.w3.org/1999/xlink"
                >
                  <desc>Created with Pixso.</desc>
                  <defs />
                  <path
                    id="Vector"
                    d="M12.17 3.88L10.61 3.88C10.19 3.88 9.94 3.4 10.11 3.02L10.11 3.02C10.27 2.64 10.36 2.27 10.36 1.92C10.36 1.21 10.1 0.53 9.63 0.06C9.23 -0.34 8.72 -0.57 8.18 -0.57L8.18 -0.57C7.22 -0.57 5.92 -0.57 4.96 -0.57L4.96 -0.57C4.37 -0.57 3.81 -0.3 3.4 0.19C3.01 0.65 2.79 1.26 2.78 1.91C2.78 2.26 2.86 2.64 3.02 3.01L3.02 3.01C3.19 3.4 2.94 3.88 2.52 3.88L1.07 3.88C0.9 3.88 0.75 3.97 0.66 4.12L-0.65 6.42C-0.81 6.69 -0.81 7.03 -0.65 7.31C-0.49 7.59 -0.2 7.75 0.12 7.75L0.12 7.75C0.65 7.75 1.09 8.17 1.12 8.69L1.2 10.1C1.2 10.46 1.35 10.79 1.61 11.01C1.88 11.24 2.23 11.34 2.57 11.28L2.57 11.28C3.11 11.21 3.58 11.63 3.59 12.17L3.59 12.79C3.59 13.05 3.8 13.26 4.06 13.26L9.84 13.26C10.1 13.26 10.31 13.05 10.31 12.79L10.31 10.35C10.31 9.67 10.67 9.07 11.14 8.58C12.07 7.59 12.58 6.18 12.64 4.37C12.65 4.24 12.6 4.12 12.51 4.03C12.42 3.94 12.3 3.88 12.17 3.88ZM4.96 0.37C5.47 0.37 5.94 0.78 6.12 1.38C6.18 1.58 6.36 1.71 6.57 1.71C6.78 1.71 6.96 1.58 7.02 1.38C7.2 0.78 7.67 0.37 8.18 0.37C8.46 0.37 8.74 0.5 8.96 0.72C9.26 1.01 9.42 1.45 9.42 1.91C9.42 2.14 9.36 2.38 9.25 2.64C9.04 3.13 8.68 3.6 8.27 4.02C8.26 4.02 8.26 4.03 8.25 4.04C8.02 4.27 7.78 4.49 7.55 4.69C6.98 5.17 6.16 5.17 5.59 4.69L5.59 4.69C4.74 3.98 4.15 3.27 3.89 2.65C3.78 2.39 3.72 2.14 3.72 1.92C3.73 1.06 4.28 0.37 4.96 0.37ZM11.17 6.87C10.82 7.63 10.3 8.19 9.6 8.6C9.46 8.68 9.37 8.84 9.37 9L9.37 10.32C9.37 11.42 8.47 12.32 7.37 12.32L5.26 12.32C4.86 12.32 4.52 11.99 4.52 11.58L4.52 11.58C4.52 11.23 4.76 10.93 5.09 10.85L5.4 10.78C5.99 10.64 6.47 10.25 6.75 9.72C7.03 9.15 7.4 8.4 7.41 8.39C7.44 8.33 7.45 8.26 7.45 8.19C7.45 8.01 7.36 7.85 7.19 7.77C6.96 7.65 6.68 7.75 6.56 7.98C6.56 7.99 6.2 8.73 5.91 9.29C5.76 9.58 5.5 9.79 5.19 9.86L3.96 10.16L2.44 10.36C2.43 10.36 2.43 10.36 2.42 10.36C2.32 10.38 2.26 10.33 2.22 10.3C2.19 10.27 2.13 10.21 2.14 10.11C2.14 10.09 2.14 10.08 2.14 10.07L2 7.62C1.99 7.51 2.02 7.39 2.02 7.28L2.02 7.28C2.02 7.02 1.81 6.81 1.55 6.81L1.55 6.81C0.95 6.81 0.57 6.17 0.87 5.65L1.06 5.32C1.23 5.01 1.56 4.82 1.92 4.82L3.52 4.82C4.04 4.82 4.54 5.04 4.95 5.38C5.65 5.98 6.27 6.37 6.32 6.4C6.4 6.45 6.49 6.47 6.57 6.47C6.66 6.47 6.74 6.45 6.82 6.4C6.87 6.37 7.5 5.97 8.21 5.36C8.6 5.03 9.08 4.82 9.58 4.82L9.58 4.82C10.71 4.82 11.65 5.82 11.18 6.84C11.18 6.85 11.17 6.86 11.17 6.87Z"
                    fill="#A3A3C5"
                    fill-opacity="1.000000"
                    fill-rule="nonzero"
                  />
                  <path
                    id="Vector"
                    d="M12.17 3.88L10.61 3.88C10.19 3.88 9.94 3.4 10.11 3.02C10.27 2.64 10.36 2.27 10.36 1.92C10.36 1.21 10.1 0.53 9.63 0.06C9.23 -0.34 8.72 -0.57 8.18 -0.57L4.96 -0.57C4.37 -0.57 3.81 -0.3 3.4 0.19C3.01 0.65 2.79 1.26 2.78 1.91C2.78 2.26 2.86 2.64 3.02 3.01C3.19 3.4 2.94 3.88 2.52 3.88L1.07 3.88C0.9 3.88 0.75 3.97 0.66 4.12L-0.65 6.42C-0.81 6.69 -0.81 7.03 -0.65 7.31C-0.49 7.59 -0.2 7.75 0.12 7.75C0.65 7.75 1.09 8.17 1.12 8.69L1.2 10.1C1.2 10.46 1.35 10.79 1.61 11.01C1.88 11.24 2.23 11.34 2.57 11.28C3.11 11.21 3.58 11.63 3.59 12.17L3.59 12.79C3.59 13.05 3.8 13.26 4.06 13.26L9.84 13.26C10.1 13.26 10.31 13.05 10.31 12.79L10.31 10.35C10.31 9.67 10.67 9.07 11.14 8.58C12.07 7.59 12.58 6.18 12.64 4.37C12.65 4.24 12.6 4.12 12.51 4.03C12.42 3.94 12.3 3.88 12.17 3.88ZM10.37 4.15Q10.49 4.18 10.61 4.18L12.17 4.18Q12.21 4.18 12.24 4.2Q12.27 4.21 12.29 4.24Q12.32 4.26 12.33 4.29Q12.34 4.32 12.34 4.36Q12.25 6.97 10.92 8.37Q10.51 8.8 10.28 9.26Q10.01 9.78 10.01 10.31Q10.01 10.33 10.01 10.35L10.01 12.79Q10.01 12.82 9.99 12.85Q9.98 12.88 9.96 12.91Q9.93 12.93 9.9 12.95Q9.87 12.96 9.84 12.96L4.06 12.96Q4.02 12.96 3.99 12.95Q3.96 12.93 3.94 12.91Q3.91 12.88 3.9 12.85Q3.89 12.82 3.89 12.79L3.89 12.17Q3.89 12.03 3.85 11.89Q3.82 11.78 3.77 11.67Q3.72 11.56 3.66 11.47Q3.58 11.36 3.48 11.27Q3.38 11.19 3.26 11.12Q3.16 11.07 3.05 11.03Q2.93 11 2.81 10.98Q2.67 10.97 2.53 10.99L2.53 10.99L2.52 10.99Q2.42 11.01 2.31 11Q2.23 10.99 2.14 10.97Q2.06 10.94 1.99 10.91Q1.89 10.86 1.81 10.79Q1.73 10.72 1.66 10.63Q1.61 10.56 1.58 10.48Q1.54 10.4 1.52 10.32Q1.5 10.22 1.5 10.11L1.5 10.1L1.42 8.68Q1.41 8.54 1.37 8.41Q1.34 8.3 1.3 8.2Q1.25 8.09 1.18 8Q1.11 7.89 1.01 7.81Q0.92 7.72 0.81 7.65Q0.72 7.59 0.61 7.55Q0.5 7.5 0.39 7.48Q0.26 7.45 0.12 7.45Q0.02 7.45 -0.07 7.42Q-0.12 7.4 -0.17 7.37Q-0.22 7.35 -0.27 7.31Q-0.34 7.24 -0.39 7.16Q-0.44 7.07 -0.46 6.98Q-0.47 6.92 -0.47 6.86Q-0.47 6.8 -0.46 6.74Q-0.44 6.65 -0.39 6.56L0.92 4.27Q0.95 4.23 0.99 4.21Q1.02 4.18 1.07 4.18L2.52 4.18Q2.64 4.18 2.76 4.15Q2.86 4.12 2.96 4.05Q3.02 4.02 3.07 3.97Q3.18 3.88 3.25 3.74Q3.3 3.66 3.33 3.57Q3.36 3.45 3.37 3.33Q3.38 3.2 3.36 3.08Q3.34 2.99 3.3 2.9Q3.08 2.38 3.08 1.91Q3.09 1.57 3.17 1.25Q3.2 1.17 3.23 1.08Q3.34 0.76 3.54 0.5Q3.58 0.44 3.63 0.38Q3.87 0.09 4.19 -0.07Q4.22 -0.09 4.24 -0.1Q4.42 -0.19 4.61 -0.23Q4.78 -0.27 4.96 -0.27L6.57 -0.27L8.18 -0.27Q8.31 -0.27 8.44 -0.24Q8.64 -0.21 8.84 -0.13Q8.89 -0.11 8.94 -0.08Q9.2 0.05 9.42 0.27Q9.47 0.32 9.52 0.38Q9.75 0.65 9.89 1.01Q9.95 1.16 9.99 1.32Q10.06 1.61 10.06 1.91Q10.06 2.38 9.83 2.9Q9.8 2.99 9.78 3.08Q9.75 3.2 9.76 3.33Q9.77 3.45 9.8 3.56Q9.83 3.66 9.88 3.74Q9.95 3.88 10.06 3.97Q10.11 4.02 10.17 4.05Q10.27 4.12 10.37 4.15ZM6.43 1.34Q6.42 1.32 6.41 1.29L6.41 1.29Q6.28 0.87 6.02 0.58Q5.95 0.5 5.86 0.42Q5.6 0.19 5.3 0.11Q5.13 0.07 4.96 0.07Q4.84 0.07 4.72 0.09Q4.53 0.13 4.34 0.23Q4.32 0.24 4.3 0.25Q4.05 0.39 3.86 0.64Q3.85 0.65 3.84 0.66Q3.65 0.91 3.54 1.22Q3.51 1.29 3.49 1.37Q3.42 1.63 3.42 1.91Q3.42 2.32 3.61 2.76Q4.04 3.78 5.39 4.92Q5.53 5.04 5.69 5.13Q5.82 5.19 5.95 5.24Q6.1 5.3 6.25 5.32Q6.41 5.35 6.57 5.35Q6.73 5.35 6.89 5.32Q7.04 5.29 7.19 5.24Q7.32 5.19 7.45 5.12Q7.61 5.04 7.75 4.92Q8.14 4.58 8.46 4.25L8.47 4.24L8.47 4.24Q8.48 4.23 8.48 4.23L8.48 4.23L8.49 4.22Q9.22 3.46 9.52 2.76Q9.72 2.31 9.72 1.91Q9.72 1.62 9.65 1.35Q9.62 1.25 9.58 1.14Q9.47 0.84 9.27 0.61Q9.22 0.55 9.18 0.51Q9 0.33 8.78 0.22Q8.75 0.2 8.72 0.19Q8.54 0.11 8.36 0.08Q8.27 0.07 8.18 0.07Q8.01 0.07 7.85 0.12Q7.54 0.19 7.28 0.42Q7.2 0.5 7.12 0.58Q6.86 0.87 6.73 1.29Q6.73 1.32 6.71 1.34Q6.69 1.36 6.67 1.38Q6.65 1.4 6.62 1.4Q6.6 1.41 6.57 1.41Q6.54 1.41 6.52 1.4Q6.49 1.4 6.47 1.38Q6.45 1.36 6.43 1.34ZM4.96 0.37C5.47 0.37 5.94 0.78 6.12 1.38C6.18 1.58 6.36 1.71 6.57 1.71C6.78 1.71 6.96 1.58 7.02 1.38C7.2 0.78 7.67 0.37 8.18 0.37C8.46 0.37 8.74 0.5 8.96 0.72C9.26 1.01 9.42 1.45 9.42 1.91C9.42 2.14 9.36 2.38 9.25 2.64C9.04 3.13 8.68 3.6 8.27 4.02C8.26 4.02 8.26 4.03 8.25 4.04C8.02 4.27 7.78 4.49 7.55 4.69C6.98 5.17 6.16 5.17 5.59 4.69C4.74 3.98 4.15 3.27 3.89 2.65C3.78 2.39 3.72 2.14 3.72 1.92C3.73 1.06 4.28 0.37 4.96 0.37ZM9.69 8.92Q9.71 8.88 9.75 8.86L9.75 8.86Q10.22 8.58 10.6 8.21Q11.11 7.7 11.44 7L11.45 6.97Q11.59 6.68 11.6 6.38Q11.61 6.21 11.58 6.05Q11.56 5.93 11.53 5.82Q11.43 5.52 11.21 5.26Q11.14 5.18 11.06 5.1Q10.82 4.87 10.5 4.72Q10.29 4.63 10.07 4.58Q9.83 4.52 9.58 4.52Q9.48 4.52 9.38 4.53Q9.05 4.56 8.74 4.69Q8.69 4.71 8.65 4.73Q8.31 4.88 8.02 5.13Q7.58 5.51 7.09 5.85Q6.84 6.03 6.66 6.15Q6.64 6.16 6.62 6.16Q6.6 6.17 6.57 6.17Q6.55 6.17 6.52 6.16Q6.5 6.16 6.48 6.15Q6.31 6.04 6.05 5.86Q5.58 5.52 5.14 5.15Q4.83 4.88 4.46 4.72Q4.43 4.71 4.39 4.69Q4.06 4.56 3.72 4.53Q3.62 4.52 3.52 4.52L1.92 4.52Q1.75 4.52 1.58 4.57Q1.42 4.61 1.27 4.7Q1.12 4.78 1 4.9Q0.88 5.02 0.8 5.17L0.61 5.5Q0.53 5.64 0.49 5.8Q0.47 5.92 0.47 6.05Q0.47 6.18 0.5 6.3Q0.54 6.44 0.61 6.57Q0.69 6.71 0.8 6.81Q0.88 6.9 0.99 6.96Q1.1 7.03 1.22 7.06Q1.38 7.11 1.55 7.11Q1.58 7.11 1.61 7.13Q1.64 7.14 1.67 7.16Q1.69 7.19 1.71 7.22Q1.72 7.25 1.72 7.28Q1.72 7.32 1.71 7.42Q1.7 7.55 1.7 7.62L1.7 7.63L1.84 10.09Q1.84 10.09 1.84 10.1Q1.83 10.19 1.86 10.27Q1.87 10.32 1.9 10.38Q1.93 10.42 1.96 10.46Q1.99 10.5 2.03 10.53Q2.07 10.57 2.11 10.59Q2.15 10.61 2.19 10.63Q2.25 10.65 2.3 10.66Q2.38 10.67 2.47 10.65L2.48 10.65L4.02 10.45L5.26 10.16Q5.4 10.12 5.54 10.06Q5.67 9.99 5.8 9.89Q5.91 9.81 6 9.7Q6.1 9.58 6.18 9.43Q6.48 8.82 6.83 8.11Q6.85 8.08 6.87 8.06Q6.9 8.04 6.93 8.03Q6.96 8.02 7 8.02Q7.03 8.02 7.06 8.04Q7.11 8.06 7.13 8.1Q7.15 8.13 7.15 8.19Q7.15 8.2 7.15 8.22Q7.15 8.24 7.14 8.26Q6.78 8.98 6.48 9.58Q6.39 9.76 6.26 9.92Q6.14 10.05 6.01 10.16Q5.86 10.28 5.7 10.36Q5.52 10.44 5.34 10.49L5.02 10.56Q4.85 10.6 4.7 10.7Q4.56 10.79 4.44 10.93Q4.33 11.07 4.28 11.23Q4.22 11.4 4.22 11.58Q4.22 11.69 4.24 11.8Q4.26 11.9 4.3 11.99Q4.34 12.07 4.39 12.15Q4.45 12.24 4.53 12.32Q4.6 12.39 4.69 12.45Q4.77 12.5 4.86 12.54Q4.95 12.58 5.04 12.6Q5.15 12.62 5.26 12.62L7.37 12.62Q7.62 12.62 7.87 12.57Q8.07 12.52 8.26 12.44Q8.46 12.36 8.63 12.24Q8.83 12.11 8.99 11.95Q9.16 11.78 9.29 11.59Q9.4 11.41 9.49 11.22Q9.57 11.02 9.61 10.82Q9.67 10.58 9.67 10.32L9.67 9Q9.67 8.95 9.69 8.92ZM11.17 6.87C10.82 7.63 10.3 8.19 9.6 8.6C9.46 8.68 9.37 8.84 9.37 9L9.37 10.32C9.37 11.42 8.47 12.32 7.37 12.32L5.26 12.32C4.86 12.32 4.52 11.99 4.52 11.58C4.52 11.23 4.76 10.93 5.09 10.85L5.4 10.78C5.99 10.64 6.47 10.25 6.75 9.72C7.03 9.15 7.4 8.4 7.41 8.39C7.44 8.33 7.45 8.26 7.45 8.19C7.45 8.01 7.36 7.85 7.19 7.77C6.96 7.65 6.68 7.75 6.56 7.98C6.56 7.99 6.2 8.73 5.91 9.29C5.76 9.58 5.5 9.79 5.19 9.86L3.96 10.16L2.44 10.36C2.43 10.36 2.43 10.36 2.42 10.36C2.32 10.38 2.26 10.33 2.22 10.3C2.19 10.27 2.13 10.21 2.14 10.11C2.14 10.09 2.14 10.08 2.14 10.07L2 7.62C1.99 7.56 2 7.49 2.01 7.43C2.01 7.38 2.02 7.33 2.02 7.28C2.02 7.02 1.81 6.81 1.55 6.81C0.95 6.81 0.57 6.17 0.87 5.65L1.06 5.32C1.23 5.01 1.56 4.82 1.92 4.82L3.52 4.82C4.04 4.82 4.54 5.04 4.95 5.38C5.65 5.98 6.27 6.37 6.32 6.4C6.4 6.45 6.49 6.47 6.57 6.47C6.66 6.47 6.74 6.45 6.82 6.4C6.87 6.37 7.5 5.97 8.21 5.36C8.6 5.03 9.08 4.82 9.58 4.82C10.71 4.82 11.65 5.82 11.18 6.84C11.18 6.85 11.17 6.86 11.17 6.87Z"
                    fill="#0E1A31"
                    fill-opacity="0.500000"
                    fill-rule="evenodd"
                  />
                </svg>
                Interests:
              </div>
              <ul class="interest_list">
                <li>Online games</li>
                <li>Sports</li>
                <li>IT</li>
                <li>Shopping</li>
              </ul>
            </div>
          </div>
        </div>
        <div class="card_item">
          <div class="right_block">
            <div class="card_img_left_list">
              <div class="web_id list_item">Web id <span>9029</span></div>
              <div class="list_item">Traffic estimate: Low</div>
              <div class="list_item">LTV estimate: Medium</div>
              <div class="list_item">Suspicious IP: 7</div>
              <div class="list_item">Suspicious emails: 7</div>
            </div>
            <img class="card_img" src="~/assets/img/cards/2.png" alt="2" />
            <div class="card_img_bottom_list">VIP users quantity: 22</div>
            <div class="card_img_right_list">
              <div class="list_item">Low social activity: 6</div>
              <div class="list_item">Multi accounts: 6</div>
              <div class="list_item">Bin mismatch: 3</div>
              <div class="list_item">Average age: 27</div>
              <div class="list_item">Average gender: Male</div>
            </div>
          </div>
          <div class="card_body">
            <h2 class="title">
              <span>Take control</span> of all incoming traffic
            </h2>
            <p class="description">
              C-SCORE analyzes both each user individually and in groups,
              allowing you to understand which traffic source attracts the most
              VIP customers and which source contains high-risk users or
              fraudulent activity
            </p>
          </div>
        </div>
        <div class="card_item">
          <div class="card_body">
            <h2 class="title"><span>Personal manager </span>and coaching</h2>
            <p class="description">
              Stay in touch with C-SCORE experts at any time. The Enterprise
              plan includes access to priority support chat, your own customer
              success manager, which helps you to use data properly and helps to
              solve shady cases
            </p>
          </div>
          <div class="right_block">
            <div class="position_imgs">
              <img
                class="setting"
                src="~/assets/img/icons/setting.svg"
                alt="setting"
              />
              <img
                class="message"
                src="~/assets/img/icons/blaknot.svg"
                alt="blaknot"
              />
              <img
                class="blaknot"
                src="~/assets/img/icons/message.svg"
                alt="message"
              />
              <img
                class="agreement"
                src="~/assets/img/icons/agreement.svg"
                alt="agreement"
              />
            </div>
            <img class="card_img" src="~/assets/img/cards/3.png" alt="3" />
          </div>
        </div>
      </div>
    </section>
    <!-- cards end -->

    <!-- free access start -->
    <FreeAccess />
    <!-- free access end -->
  </main>
</template>

<script>
export default {
  data() {
    return {
      filter: true,
      growing: [
        {
          id: 1,
          tarif: "Free",
          sum: 0,
          lifetime: "forever",
          list: [
            "3 users",
            "Basic rules",
            "700 manual checkups",
            "Email support",
          ],
        },
        {
          id: 2,
          tarif: "Basic",
          sum: 399,
          lifetime: "month",
          list: [
            "10 users",
            "Adopted rules to your business",
            "1200 API calls/month",
            "Email support (response within 24 hours)",
            "Api integration",
          ],
        },
        {
          id: 3,
          tarif: "Pro",
          sum: 2100,
          lifetime: "month",
          list: [
            "Unlimited users",
            "Adopted C-SCORE rules and custom rules",
            "30000 API Calls",
            "Personal manager and technical support",
            "Api integration",
          ],
        },
      ],
      enterprise: [
        {
          id: 1,
          title: "Non-doc verification",
          description:
            "Onboard users all over the globe with using our Non-doc verification method using only email and phone number",
          list: [
            "Digital footprint and social activity",
            "Confirm gender, age information and geolocation",
            "Learn about the user's interests",
          ],
        },
        {
          id: 2,
          title: "Social Rate",
          description:
            "Learn everything about your client: get their psychological profile, social status and information about their ability to pay",
          list: [
            "200+ rules and patterns forming social rating and determining solvency",
            "AI-based detailed psychological profile",
          ],
        },
        {
          id: 3,
          title: "Anti-fraud system",
          description:
            "Instantly detect fraudulent activity at all stages of the user journey. Analyze fraudulent activity across every source or group",
          list: [
            "Multi-accounting & Bonus abuse",
            "Chargebacks & Money laundering",
            "User & Group fraud score",
            "Learning machine",
          ],
        },
        {
          id: 4,
          title: "Affiliate partners’ scoring & analysis",
          description:
            "Gain control over your partner network. Utilize group scoring and forecast profitability to enhance traffic lifetime value (LTV) and quality",
          list: [
            "Group Social Rate & LTV analysis",
            "Beat affiliated partners multi accounting",
            "Early stage traffic profitability forecast",
            "Case management",
          ],
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
// home start
.home {
  background-image: url("~/assets/img/home-bg.png");
  background-repeat: no-repeat;
  background-size: 100%;
  padding: 200px 0 107px;
  background-color: #010e26;
  .title {
    font-size: 50px;
    font-weight: 400;
    line-height: 66px;
    letter-spacing: 0%;
    text-align: center;
    color: rgb(255, 255, 255);
    margin-bottom: 30px;
    span {
      color: rgb(64, 87, 217);
    }
  }
  .description {
    color: rgb(163, 163, 197);
    font-size: 14px;
    font-weight: 400;
    line-height: 25.2px;
    letter-spacing: 0%;
    text-align: center;
    margin-bottom: 62px;
  }
  .home_filter_btns {
    display: flex;
    justify-content: center;
    margin-bottom: 90px;
    button {
      padding: 22px 96px;
      border-bottom: 1px solid rgb(106, 106, 165);
      color: rgb(106, 106, 165);
      font-size: 16px;
      font-weight: 500;
      line-height: 24px;
      letter-spacing: 1.3px;
      text-align: center;
      transition: 0.3s;
      &:hover {
        color: rgb(255, 255, 255);
      }
    }
    .active {
      color: rgb(255, 255, 255);
    }
  }
  .growing_container {
    display: none;
    grid-template-columns: repeat(3, 1fr);
    gap: 32px;
    visibility: hidden;
    transform: translateY(200px);
    opacity: 0;
    transition: 0.3s;
    .growing_card {
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: 10px;
      backdrop-filter: blur(15px);
      background: rgba(255, 255, 255, 0.05);
      padding: 32px 37px;
      position: relative;
      transition: 0.3s;
      cursor: pointer;
      &:hover {
        box-shadow: 0px 0px 10.6px 0px rgba(64, 87, 217, 0.7);
      }
      .tariff {
        color: rgb(255, 255, 255);
        font-size: 20px;
        font-weight: 400;
        line-height: 24px;
        letter-spacing: 0%;
        text-align: left;
        margin-bottom: 30px;
      }
      .growing_amount {
        display: flex;
        align-items: start;
        gap: 4px;
        margin-bottom: 37px;
        .valute_icon {
          margin-top: -12px;
          color: rgb(255, 255, 255);
          font-size: 20px;
          font-weight: 400;
          line-height: 24px;
          letter-spacing: 0%;
          text-align: left;
        }
        .right_block {
          display: flex;
          align-items: end;
          gap: 5px;
          color: rgb(255, 255, 255);
          font-size: 24px;
          font-weight: 400;
          line-height: 24px;
          letter-spacing: 0%;
          text-align: left;
          .growing_sum {
            font-size: 64px;
            line-height: 48px;
          }
        }
      }
      .growing_list {
        padding-bottom: 70px;
        .list_item {
          display: flex;
          align-items: start;
          gap: 15px;
          margin-bottom: 15px;
          &:last-child {
            margin-bottom: 0;
          }
          span {
            color: rgb(163, 163, 197);
            font-size: 14px;
            font-weight: 400;
            line-height: 15px;
            letter-spacing: 0%;
            text-align: left;
            color: rgb(163, 163, 197);
          }
        }
      }
      .growing_link {
        width: 40px;
        height: 40px;
        display: flex;
        align-items: center;
        justify-content: center;
        position: absolute;
        bottom: 32px;
        right: 37px;
        border-radius: 100%;
        background: rgba(255, 255, 255, 0.1);
        transition: 0.3s;
        &:hover {
          transform: scale(1.2);
        }
      }
    }
  }
  .enterprise_container {
    display: none;
    visibility: hidden;
    transform: translateY(200px);
    opacity: 0;
    transition: 0.3s;
    .enterprise_plan {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 85px;
      align-items: center;
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: 10px;
      backdrop-filter: blur(15px);
      background: rgba(255, 255, 255, 0.05);
      padding: 56px 45px;
      margin-bottom: 54px;
      .card_left {
        .head {
          color: rgb(64, 87, 217);
          font-size: 16px;
          font-weight: 400;
          line-height: 24px;
          letter-spacing: 0%;
          text-align: left;
          margin-bottom: 4px;
        }
        .title {
          color: rgb(255, 255, 255);
          font-size: 32px;
          font-weight: 400;
          line-height: 53px;
          letter-spacing: 0%;
          text-align: left;
          margin-bottom: 20px;
        }
        .description {
          color: rgb(163, 163, 197);
          font-size: 16px;
          font-weight: 400;
          line-height: 25.2px;
          letter-spacing: 0%;
          text-align: left;
          margin-bottom: 41px;
        }
        .start_free_btn {
          max-width: 345px;
          width: 100%;
          margin: 0 auto;
          padding: 22px;
          border-radius: 5px;
          background: rgb(247, 147, 30);
          border: 1px solid rgb(247, 147, 30);
          color: rgb(255, 255, 255);
          font-size: 16px;
          font-weight: 500;
          line-height: 24px;
          letter-spacing: 0.5px;
          text-align: center;
          text-transform: uppercase;
          transition: 0.3s;
          &:hover {
            background-color: transparent;
            color: rgb(247, 147, 30);
          }
        }
      }
      .card_list {
        .list_item {
          display: flex;
          align-items: start;
          gap: 15px;
          color: rgb(163, 163, 197);
          font-size: 16px;
          font-weight: 400;
          line-height: 22.4px;
          letter-spacing: 0%;
          text-align: left;
          margin-bottom: 24px;
        }
        .start_free_btn {
          display: none;
          max-width: 345px;
          width: 100%;
          margin: 0 auto;
          padding: 22px;
          border-radius: 5px;
          background: rgb(247, 147, 30);
          color: rgb(255, 255, 255);
          font-size: 16px;
          font-weight: 500;
          line-height: 24px;
          letter-spacing: 0.5px;
          text-align: center;
          text-transform: uppercase;
        }
      }
    }
    .enterprise_cards {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 30px;
      .card_item {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 30px;
        padding: 32px;
        border: 1px solid rgba(255, 255, 255, 0.1);
        border-radius: 10px;
        backdrop-filter: blur(15px);
        background: rgba(255, 255, 255, 0.05);
        .card_left {
          .title {
            color: rgb(255, 255, 255);
            font-family: Inter;
            font-size: 24px;
            font-weight: 400;
            line-height: 35px;
            letter-spacing: 0%;
            text-align: left;
            margin-bottom: 12px;
          }
          .description {
            color: rgb(163, 163, 197);
            font-size: 14px;
            font-weight: 400;
            line-height: 25.2px;
            letter-spacing: 0%;
            text-align: left;
            margin-bottom: 0;
          }
        }
        .list_item {
          display: flex;
          align-items: start;
          gap: 15px;
          color: rgb(163, 163, 197);
          font-family: Inter;
          font-size: 14px;
          font-weight: 400;
          line-height: 25px;
          letter-spacing: 0%;
          text-align: left;
          list-style: none;
          .circle {
            display: block;
            min-width: 7.5px;
            min-height: 7.5px;
            background: rgb(64, 87, 217);
            border-radius: 100%;
            margin-top: 9px;
          }
        }
      }
    }
  }
  .growing_active {
    display: grid;
    visibility: visible;
    transform: translateY(0);
    opacity: 1;
  }
  .enterprise_active {
    display: block;
    visibility: visible;
    transform: translateY(0);
    opacity: 1;
  }
}
// home end

// cards start
.cards {
  position: relative;
  padding: 20px 0;
  background: url("~/assets/img/cards/cards_bg.png");
  background-repeat: no-repeat;
  background-size: cover;
  .card_item {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 60px;
    padding: 60px 0;
    position: relative;
    z-index: 2;
    &:hover {
      .right_block {
        .card_img {
          transform: scale(1.2);
        }
      }
    }

    .card_body {
      padding: 72px 0 80px;
      .title {
        font-size: 50px;
        font-weight: 500;
        line-height: 60px;
        letter-spacing: 0%;
        text-align: left;
        margin-bottom: 16px;
        color: rgb(255, 255, 255);
        span {
          color: rgb(64, 87, 217);
        }
      }
      .description {
        max-width: 492px;
        color: rgb(163, 163, 197);
        font-family: Inter, sans-serif;
        font-size: 16px;
        font-weight: 400;
        line-height: 28px;
        letter-spacing: 0%;
        text-align: left;
      }
    }
    .right_block {
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
      .about_user {
        position: absolute;
        top: 0;
        left: 0;
        z-index: 2;
        width: 184.4px;
        padding: 35px 13px 23px 20px;
        background: url("~/assets/img/cards/user_block.svg");
        background-size: cover;

        .name {
          color: rgb(255, 255, 255);
          font-family: Inter;
          font-size: 16px;
          font-weight: 400;
          line-height: 19px;
          letter-spacing: 0%;
          text-align: left;
          margin-bottom: 14px;
        }
        .social_rate {
          color: rgb(163, 163, 197);
          font-family: Inter;
          font-size: 14px;
          font-weight: 400;
          line-height: 13px;
          letter-spacing: 0%;
          text-align: left;
          span {
            font-size: 27px;
            line-height: 36px;
          }
        }
        .safe {
          display: flex;
          align-items: center;
          gap: 4px;
          color: rgb(242, 128, 39);
          font-size: 12px;
          font-weight: 400;
          line-height: 16.8px;
          letter-spacing: 0%;
          text-align: left;
          margin-bottom: 16px;
          span {
            width: 5.76px;
            height: 5.76px;
            border-radius: 100%;
            background: rgb(242, 128, 39);
          }
        }
        .list_item {
          display: flex;
          align-items: center;
          gap: 8px;
          color: rgb(163, 163, 197);
          font-family: Inter;
          font-size: 12px;
          font-weight: 400;
          line-height: 125%;
          letter-spacing: 0%;
          text-align: left;
          margin-bottom: 15px;
          &:last-child {
            margin-bottom: 0;
          }
        }
      }
      .interest {
        position: absolute;
        bottom: 40px;
        right: 46px;
        z-index: 2;
        width: 130.34px;
        border: 1px solid rgba(255, 255, 255, 0.1);
        border-radius: 2px;
        box-shadow: 0px 0px 10.6px 0px rgba(64, 87, 217, 0.7);
        backdrop-filter: blur(15px);
        background: rgba(7, 24, 54, 0.6);
        padding: 26px 9.3px 22px 14.2px;
        clip-path: polygon(
          99.406% 5.856%,
          99.406% 98.95%,
          99.406% 98.95%,
          99.396% 99.052%,
          99.365% 99.149%,
          99.316% 99.239%,
          99.25% 99.322%,
          99.169% 99.395%,
          99.075% 99.458%,
          98.968% 99.509%,
          98.852% 99.548%,
          98.727% 99.572%,
          98.596% 99.58%,
          1.081% 99.58%,
          1.081% 99.58%,
          0.95% 99.572%,
          0.825% 99.548%,
          0.708% 99.509%,
          0.602% 99.458%,
          0.508% 99.395%,
          0.427% 99.322%,
          0.361% 99.239%,
          0.312% 99.149%,
          0.281% 99.052%,
          0.27% 98.95%,
          0.27% 0.84%,
          0.27% 0.84%,
          0.281% 0.738%,
          0.312% 0.641%,
          0.361% 0.551%,
          0.427% 0.468%,
          0.508% 0.395%,
          0.602% 0.332%,
          0.708% 0.28%,
          0.825% 0.242%,
          0.95% 0.218%,
          1.081% 0.21%,
          24.919% 0.21%,
          41.447% 0.21%,
          41.447% 0.21%,
          41.503% 0.212%,
          41.558% 0.216%,
          41.612% 0.223%,
          41.665% 0.233%,
          41.717% 0.246%,
          41.768% 0.261%,
          41.818% 0.28%,
          41.866% 0.3%,
          41.912% 0.324%,
          41.956% 0.35%,
          49.372% 4.993%,
          49.372% 4.993%,
          49.446% 5.036%,
          49.523% 5.075%,
          49.603% 5.11%,
          49.685% 5.14%,
          49.77% 5.166%,
          49.857% 5.187%,
          49.946% 5.204%,
          50.036% 5.216%,
          50.127% 5.223%,
          50.22% 5.226%,
          98.596% 5.226%,
          98.596% 5.226%,
          98.727% 5.234%,
          98.852% 5.258%,
          98.968% 5.296%,
          99.075% 5.347%,
          99.169% 5.41%,
          99.25% 5.484%,
          99.316% 5.566%,
          99.365% 5.657%,
          99.396% 5.754%,
          99.406% 5.856%
        );
        .interest_top {
          color: rgb(163, 163, 197);
          font-family: Inter;
          font-size: 14px;
          font-weight: 500;
          line-height: 17px;
          letter-spacing: 0%;
          text-align: left;
          margin-bottom: 5px;
        }
        .interest_list {
          padding-left: 24px;
          color: rgb(163, 163, 197);
          font-family: Inter;
          font-size: 11px;
          font-weight: 400;
          line-height: 13px;
          letter-spacing: 0%;
          text-align: left;
          li {
            list-style-type: disc;
          }
        }
      }
      .card_img_left_list {
        display: flex;
        flex-direction: column;
        align-items: start;
        position: absolute;
        left: 10px;
        top: 0;
        z-index: 2;

        .list_item {
          box-sizing: border-box;
          border: 1px solid rgba(255, 255, 255, 0.1);
          backdrop-filter: blur(15px);
          background: rgba(7, 24, 54, 0.65);
          padding: 6px 21px 6px 21px;
          color: rgb(163, 163, 197);
          font-family: Inter;
          font-size: 12px;
          font-weight: 400;
          line-height: 15px;
          letter-spacing: 0%;
          text-align: left;
          &:nth-child(2) {
            margin-bottom: 21px;
            margin-left: 23px;
          }
          &:nth-child(3) {
            margin-bottom: 24px;
          }
          &:nth-child(4) {
            margin-bottom: 28px;
            margin-left: 7px;
          }
          &:last-child {
            margin-left: 21px;
          }
        }
        .web_id {
          margin-bottom: 30px;
          width: 170px;
          height: 90px;
          display: flex;
          align-items: center;
          justify-content: center;
          margin-left: 12%;
          gap: 7px;
          background: url("~/assets/img/cards/web_id.svg");
          background-repeat: no-repeat;
          background-size: cover;
          padding: 0;
          border: 0;
          box-shadow: none;
          backdrop-filter: blur(0);
          font-family: Inter;
          font-size: 16px;
          font-weight: 400;
          line-height: 0px;
          letter-spacing: 0%;
          text-align: center;
          span {
            line-height: 20px;
            font-size: 20px;
            color: rgb(255, 255, 255);
          }
        }
      }
      .card_img_right_list {
        display: flex;
        flex-direction: column;
        align-items: end;
        position: absolute;
        right: 9px;
        top: 46px;
        z-index: 2;
        .list_item {
          box-sizing: border-box;
          border: 1px solid rgba(255, 255, 255, 0.1);
          backdrop-filter: blur(15px);
          background: rgba(7, 24, 54, 0.65);
          padding: 6px 21px 6px 21px;
          color: rgb(163, 163, 197);
          font-family: Inter;
          font-size: 12px;
          font-weight: 400;
          line-height: 15px;
          letter-spacing: 0%;
          text-align: left;
          white-space: nowrap;
          &:nth-child(1) {
            margin-bottom: 29px;
            margin-right: 25%;
          }
          &:nth-child(2) {
            margin-bottom: 34px;
            margin-right: 28px;
          }
          &:nth-child(3) {
            margin-bottom: 37px;
          }
          &:nth-child(4) {
            margin-bottom: 35px;
          }
          &:last-child {
            margin-right: 3px;
          }
        }
      }
      .card_img_bottom_list {
        position: absolute;
        left: 50%;
        bottom: 32px;
        z-index: 2;
        transform: translateX(-50%);
        box-sizing: border-box;
        border: 1px solid rgba(255, 255, 255, 0.1);
        backdrop-filter: blur(15px);
        background: rgba(7, 24, 54, 0.65);
        padding: 6px 21px 6px 21px;
        color: rgb(163, 163, 197);
        font-family: Inter;
        font-size: 12px;
        font-weight: 400;
        line-height: 15px;
        letter-spacing: 0%;
        text-align: left;
      }
      .setting {
        position: absolute;
        top: 16px;
        left: 68px;
        z-index: 2;
      }
      .blaknot {
        position: absolute;
        left: 0;
        bottom: 14px;
        z-index: 2;
      }
      .message {
        position: absolute;
        top: 32px;
        right: 36px;
        z-index: 2;
      }
      .agreement {
        position: absolute;
        right: 24px;
        bottom: 51px;
        z-index: 2;
      }
      .card_img {
        transition: 0.3s;
      }
    }
  }
}
// cards end

@media (max-width: 992px) {
  .home {
    .growing_container {
      grid-template-columns: repeat(2, 1fr);
      .growing_card {
        &:last-child {
          grid-column: 1/3;
        }
      }
    }
    .enterprise_container {
      .enterprise_plan {
        gap: 30px;
      }
      .enterprise_cards {
        .card_item {
          grid-template-columns: repeat(1, 1fr);
          gap: 20px;
        }
      }
    }
  }
  .cards {
    .card_item {
      display: flex;
      flex-direction: column;
      gap: 30px;
      .card_body {
        order: 2;
        padding: 0;
        .title {
          br {
            display: none;
          }
        }
        .description {
          max-width: 100%;
        }
      }
      .right_block {
        width: 100%;
        max-width: 540px;
        min-height: 388px;
        height: 100%;
        margin: 0 auto;
        order: 1;
      }
    }
  }
}
@media (max-width: 768px) {
  .home {
    .home_filter_btns {
      margin-bottom: 50px;
    }
    .growing_container {
      grid-template-columns: repeat(1, 1fr);
      .growing_card {
        padding: 20px;
        &:last-child {
          grid-column: auto;
        }
        .growing_list {
          padding-bottom: 40px;
        }
      }
    }
    .enterprise_container {
      .enterprise_plan {
        display: flex;
        flex-direction: column;
        align-items: start;
        gap: 30px;
        padding: 30px;
        .card_left {
          .description {
            margin-bottom: 20px;
          }
          .start_free_btn {
            display: none;
          }
        }
        .card_list {
          .start_free_btn {
            display: block;
            margin: 0;
            margin-top: 40px;
          }
        }
      }
      .enterprise_cards {
        gap: 20px;
        .card_item {
          grid-template-columns: repeat(1, 1fr);
          gap: 20px;
          padding: 20px;
        }
      }
    }
  }
}
@media (max-width: 576px) {
  .home {
    padding: 120px 0 50px;
    .title {
      font-size: 36px;
      margin-bottom: 20px;
      line-height: 40px;
    }
    .description {
      font-size: 12px;
      line-height: 18px;
      margin-bottom: 40px;
    }
    .home_filter_btns {
      margin-bottom: 30px;
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      button {
        padding: 18px;
        font-size: 14px;
      }
    }
    .growing_container {
      .growing_card {
        .tariff {
          font-size: 18px;
        }
        .growing_amount {
          margin-bottom: 30px;
          .valute_icon {
            font-size: 18px;
          }
          .right_block {
            font-size: 20px;
            .growing_sum {
              font-size: 50px;
              line-height: 35px;
            }
          }
        }
        .growing_list {
          .list_item {
            gap: 10px;
            margin-bottom: 10px;
            img {
              height: 15px;
            }
            span {
              font-size: 12px;
            }
          }
        }
        .growing_link {
          width: 35px;
          height: 35px;
          bottom: 20px;
          right: 20px;
        }
      }
    }
    .enterprise_container {
      .enterprise_plan {
        gap: 20px;
        padding: 10px;
        margin-bottom: 20px;
        .card_left {
          .head {
            font-size: 12px;
          }
          .title {
            font-size: 20px;
            line-height: 35px;
          }
          .description {
            margin-bottom: 8px;
            font-size: 12px;
            line-height: 18px;
          }
          .start_free_btn {
            display: none;
          }
        }
        .card_list {
          .list_item {
            font-size: 12px;
            margin-bottom: 8px;
          }
          .start_free_btn {
            display: block;
            margin: 0;
            margin-top: 20px;
            font-size: 12px;
            padding: 10px;
          }
        }
      }
      .enterprise_cards {
        grid-template-columns: repeat(1, 1fr);
        gap: 10px;
        .card_item {
          grid-template-columns: repeat(1, 1fr);
          gap: 10px;
          padding: 10px;
          .card_left {
            .title {
              font-size: 16px;
              line-height: 20px;
              margin-bottom: 10px;
            }
            .description {
              font-size: 12px;
              line-height: 15px;
              margin-bottom: 10px;
            }
          }
          .list_item {
            font-size: 12px;
            line-height: 20px;
            gap: 10px;
            .circle {
              min-width: 6px;
              min-height: 6px;
              margin-top: 7px;
            }
          }
        }
      }
    }
  }
  .cards {
    .card_item {
      padding-bottom: 20px;
      .right_block {
        .about_user {
          width: 166.4px;
          .name {
            font-size: 12px;
            margin-bottom: 8px;
          }
          .social_rate {
            font-size: 10px;
            span {
              font-size: 18px;
            }
          }
          .safe {
            font-size: 8px;
            margin-bottom: 8px;
          }
          .list_item {
            font-size: 8px;
            margin-bottom: 8px;
          }
          .age {
            img {
              height: 13px;
            }
          }
          .gender {
            img {
              height: 14px;
            }
          }
          .country {
            img {
              height: 13px;
            }
          }
        }
        .interest {
          right: 0;
          bottom: 20px;
          padding: 16px 8px 15px 10px;
          .interest_top {
            font-size: 12px;
          }
          .interest_list {
            font-size: 9px;
          }
        }
        .card_img_left_list {
          top: 32px;
          left: 0;
          .list_item {
            padding: 4px 15px;
            font-size: 9px;
            line-height: 12px;
          }
          .web_id {
            width: 129px;
            height: 67px;
            font-size: 12px;
            span {
              line-height: 16px;
              font-size: 16px;
            }
          }
        }
        .card_img_right_list {
          right: 0;
          .list_item {
            padding: 4px 15px;
            font-size: 9px;
            line-height: 12px;
          }
        }
        .card_img_bottom_list {
          padding: 4px 15px;
          font-size: 9px;
          line-height: 12px;
          bottom: 38px;
        }
        .setting {
          height: 55px;
        }
        .message {
          height: 85px;
        }
        .blaknot {
          height: 75px;
        }
        .agreement {
          height: 65px;
        }
      }
      .card_body {
        .title {
          font-size: 28px;
          line-height: 35px;
          margin-bottom: 10px;
        }
        .description {
          font-size: 12px;
          line-height: 18px;
        }
      }
    }
  }
}
</style>
