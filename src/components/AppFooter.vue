<script>

export default {
  data() {
    return {

      footerColumns: [
        {
          title: 'DC COMICS',
          links: [
            'Characters',
            'Comics',
            'Movies',
            'TV',
            'Games',
            'Videos',
            'News',
          ]
        },
        {
          title: 'SHOP',
          links: [
            'Shop DC',
            'Shop DC Collectibles',
          ],
        },
        {
          title: 'DC',
          links: [
            'Terms of Use',
            'Provacy Policy (New)',
            'Ad Choices',
            'Advertising',
            'Jobs',
            'Subscriptions',
            'Talent Workshops',
            'CPSC Certificates',
            'Ratings',
            'Shop Help',
            'Contact Us',
          ]
        },
        {
          title: 'SITES',
          links: [
            'DC',
            'MAD Magazine',
            'DC Kids',
            'DC Universe',
            'DC Power Visa',
          ]
        },
      ],

      socials: [
        '/images/footer-facebook.png',
        '/images/footer-twitter.png',
        '/images/footer-youtube.png',
        '/images/footer-pinterest.png',
        '/images/footer-periscope.png',
      ]
    }
  }
}

</script>

<template>
  <footer>
    <div class="footer-container">
      <div class="footer-up container-centered">
        <div v-for="footerColumn in footerColumns" class="footer-links">
          <strong> {{ footerColumn.title }} </strong>
          <ul>
            <li v-for="link in footerColumn.links"> {{ link }}</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="footer-down container-centered">
      <button class="btn sign-up"><strong>SIGN-UP NOW!</strong></button>

      <div class="socials">
        <h3>FOLLOW US</h3>
        <ul>
          <li v-for="social in socials">
            <img :src="social" alt="">
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<style lang='scss' scoped>
footer {
  background-color: #303030;

  .footer-container {
    width: 100%;
    background-image: url(/images/footer-bg.jpg);
    background-size: cover;

    .footer-up {
      background-image: url(/images/dc-logo-bg.png);
      background-repeat: no-repeat;
      background-position: right;
      height: 380px;
      padding: 60px 0;
      display: flex;
      flex-direction: column;
      flex-wrap: wrap;
      align-content: flex-start;
      gap: 30px;

      li {
        font-size: .8em;
        color: #959595;

        &:hover {
          cursor: pointer;
          text-decoration: underline;
        }
      }
    }
  }

  .footer-down {
    padding: 30px 0;
    display: flex;
    justify-content: space-between;
    align-items: center;

    .socials {
      display: flex;
      align-items: center;
      gap: 30px;

      h3 {
        color: #0282f9;
      }

      ul {
        display: flex;
        gap: 10px;
      }
    }

  }
}
</style>