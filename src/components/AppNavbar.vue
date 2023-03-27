<script>

export default {
  data() {
    return {

      links: [
        'characters',
        'comics',
        'movies',
        'tv',
        'games',
        'collectibles',
        'videos',
        'fans',
        'news',
        'shop',
      ]

    }
  }
}
</script>

<template>
  <nav>
    <div class="navbar-container container-centered">

      <div class="logo">
        <img src="/images/dc-logo.png" alt="DC Logo">
      </div>
      <div class="links">
        <ul>
          <li v-for="link in links"><strong>{{ link }}</strong></li>
        </ul>
      </div>

    </div>
  </nav>
</template>

<style lang='scss' scoped>
nav {
  background-color: white;
  color: #464646;

  .navbar-container {
    display: flex;
    justify-content: space-between;
    align-items: center;

    .logo {
      padding: 10px 0;
      display: flex;


      img {
        width: 70px;
      }
    }

    .links ul {
      display: flex;
      flex-direction: row;
      gap: 20px;

      li {
        text-transform: uppercase;
        font-size: .8em;

        &:hover {
          cursor: pointer;
          color: #0282f9;
        }
      }
    }
  }

}
</style>