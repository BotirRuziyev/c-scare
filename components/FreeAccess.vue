<template>
  <div class="free_access d-flex flex-column align-center">
    <p class="description"><span>Reveal</span> your clients’ potential</p>
    <nuxt-link to="#" class="free_access_link"
      >Get 30 days access for free</nuxt-link
    >
  </div>
</template>

<style lang="scss" scoped>
.free_access {
  background: rgb(255, 255, 255);
  padding: 90px 20px 73px;
  .description {
    font-size: 50px;
    font-weight: 500;
    line-height: 60px;
    letter-spacing: 0%;
    text-align: left;
    color: rgb(0, 17, 51);
    text-align: center;
    margin-bottom: 38px;
    span {
      color: rgb(64, 87, 217);
    }
  }
  .free_access_link {
    padding: 22px 45px;
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
    cursor: pointer;
    transition: 0.3s;
    &:hover {
      background-color: transparent;
      color: rgb(247, 147, 30);
    }
  }
}
@media (max-width: 768px) {
  .free_access {
    padding: 50px 20px;
    .description {
      font-size: 28px;
      line-height: 32px;
      margin-bottom: 25px;
    }
    .free_access_link {
      font-size: 12px;
      padding: 15px 30px;
    }
  }
}
</style>
