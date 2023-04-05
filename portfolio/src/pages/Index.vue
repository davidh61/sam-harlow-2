<template>
  <Layout>

    <body>
      <div class="header-container">
        <h1>Sam Harlow</h1>
        <svg class="arrows" @click="scrollToPortfolio">
          <path class="a1" d="M0 0 L30 32 L60 0"></path>
          <path class="a2" d="M0 20 L30 52 L60 20"></path>
          <path class="a3" d="M0 40 L30 72 L60 40"></path>
        </svg>
      </div>
      <div class="portfolio-container" id="portfolio">
        <h2>Portfolio</h2>
        <div class="portfolio-content">
          <video src="@/assets/VID-20230405-WA0000.mp4" controls></video>
        </div>
      </div>
    </body>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Hello, world!'
  },
  methods: {
    scrollToPortfolio(event) {
      document.getElementById('portfolio').scrollIntoView({block: 'end', behavior: 'smooth'})
    }
  }
}
</script>

<style lang="scss">
body {
  overflow-x: hidden;
  margin: 0;
  padding: 0;
  font-family: 'Raleway', sans-serif;
  background-color: #000;

  .header-container {
    height: 100vh;
    width: 100vw;
    display: flex;
    justify-content: center;
    align-items: center;

    h1 {
      margin: 0;
      font-size: 150px;
      color: rgba(225, 225, 225, .01);
      background-image: url("https://images.unsplash.com/photo-1499195333224-3ce974eecb47?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=2cf549433129d4227d1879347b9e78ce&auto=format&fit=crop&w=1248&q=80");
      background-repeat: repeat;
      -webkit-background-clip: text;
      animation: animate 15s ease-in-out infinite;
      text-align: center;
      text-transform: uppercase;
      font-weight: 900;

      @media only screen and (max-width: 768px) {
        font-size: 75px;
      }
    }


    .arrows {
      width: 60px;
      height: 72px;
      position: absolute;
      left: 50%;
      margin-left: -30px;
      bottom: 20px;

      :hover {
        cursor: pointer;
      }
    }

    .arrows path {
      stroke: #2994D1;
      fill: transparent;
      stroke-width: 1px;
      animation: arrow 2s infinite;
      -webkit-animation: arrow 2s infinite;
    }

    @keyframes arrow {
      0% {
        opacity: 0
      }

      40% {
        opacity: 1
      }

      80% {
        opacity: 0
      }

      100% {
        opacity: 0
      }
    }

    @-webkit-keyframes arrow

    /*Safari and Chrome*/
      {
      0% {
        opacity: 0
      }

      40% {
        opacity: 1
      }

      80% {
        opacity: 0
      }

      100% {
        opacity: 0
      }
    }

    .arrows path.a1 {
      animation-delay: -1s;
      -webkit-animation-delay: -1s;
      /* Safari 和 Chrome */
    }

    .arrows path.a2 {
      animation-delay: -0.5s;
      -webkit-animation-delay: -0.5s;
      /* Safari 和 Chrome */
    }

    .arrows path.a3 {
      animation-delay: 0s;
      -webkit-animation-delay: 0s;
      /* Safari 和 Chrome */
    }
  }

  .portfolio-container {
    // border: white 1px solid;
    height: 100vh;
    width: 100vw;
    display: flex;
    justify-content: center;
    padding-top: 25px;
    flex-direction: column;

    h2 {
      margin: 0;
      font-size: 50px;
      color: rgba(225, 225, 225, .01);
      background-image: url("https://images.unsplash.com/photo-1499195333224-3ce974eecb47?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=2cf549433129d4227d1879347b9e78ce&auto=format&fit=crop&w=1248&q=80");
      background-repeat: repeat;
      -webkit-background-clip: text;
      animation: animate 15s ease-in-out infinite;
      text-align: center;
      text-transform: uppercase;
      font-weight: 900;
      margin-bottom: 150px;
    }

    .portfolio-content {
      text-align: center;
    }


  }

  @keyframes animate {

    0%,
    100% {
      background-position: left top;
    }

    25% {
      background-position: right bottom;
    }

    50% {
      background-position: left bottom;
    }

    75% {
      background-position: right top;
    }
  }
}</style>
