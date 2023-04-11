<template>
  <Layout>
      <div class="header-container">
        <h1>Sam Harlow</h1>
        <svg class="arrows" v-on:click="scrollToPortfolio">
          <path class="a1" d="M0 0 L30 32 L60 0"></path>
          <path class="a2" d="M0 20 L30 52 L60 20"></path>
          <path class="a3" d="M0 40 L30 72 L60 40"></path>
        </svg>
      </div>
      <div class="portfolio-container" id="portfolio">
        <h2>SHOWREEL</h2>
        <div class="portfolio-content">
          <video src="@/assets/VID-20230405-WA0000.mp4" controls></video>
        </div>
      </div>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Hello, world!'
  },
  methods: {
    scrollToPortfolio(event) {
      alert('Hello world')
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
  background-image: linear-gradient(white, pink, black);

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
      background-image: url("https://blog.stockvault.net/wp-content/uploads/2020/02/preview-309.jpg");
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
      background-image: url("https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/597f3433-65c0-46e3-9ea6-ad5a23ca5e80/ddbhprw-d2a12686-f609-47b3-aae3-a1aa28f09c25.png/v1/fill/w_1280,h_848,q_80,strp/_textures_grunge___scratches_by_iguessitsnick_ddbhprw-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9ODQ4IiwicGF0aCI6IlwvZlwvNTk3ZjM0MzMtNjVjMC00NmUzLTllYTYtYWQ1YTIzY2E1ZTgwXC9kZGJocHJ3LWQyYTEyNjg2LWY2MDktNDdiMy1hYWUzLWExYWEyOGYwOWMyNS5wbmciLCJ3aWR0aCI6Ijw9MTI4MCJ9XV0sImF1ZCI6WyJ1cm46c2VydmljZTppbWFnZS5vcGVyYXRpb25zIl19.tZptKiv27MzUm1XAQ5lHanM00ShugI3CJcCTOQh2lz0");
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
