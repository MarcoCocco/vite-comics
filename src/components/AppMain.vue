<script>

export default {
  data() {
    return {

      mainLinks: [

        {
          image: '/images/buy-comics-digital-comics.png',
          name: 'DIGITAL COMICS',
        },
        {
          image: '/images/buy-comics-merchandise.png',
          name: 'DC MERCHANDISE',
        },
        {
          image: '/images/buy-comics-subscriptions.png',
          name: 'SUBSCRIPTION',
        },
        {
          image: '/images/buy-comics-shop-locator.png',
          name: 'COMIC SHOPO LOCATOR',
        },
        {
          image: '/images/buy-dc-power-visa.svg',
          name: 'DC POWER VISA',
        },

      ]
    }
  }
}

</script>

<template>
  <main>
    <div class="main-container container-centered">
      <div class="main-links">
        <ul>
          <li v-for="mainLink in mainLinks"><img :src="mainLink.image" alt="">{{ mainLink.name }}</li>
        </ul>
      </div>
    </div>
  </main>
</template>

<style lang='scss' scoped>
main {
  background-color: #0282f9;

  .main-container {

    .main-links {

      ul {
        padding: 40px;
        display: flex;
        justify-content: space-around;
        gap: 40px;

        li {
          display: flex;
          align-items: center;
          gap: 10px;

          img {
            height: 50px;
          }

          &:hover {
            cursor: pointer;
            text-decoration: underline;
          }

        }
      }
    }
  }
}
</style>