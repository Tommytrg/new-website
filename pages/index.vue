<template>
  <div>
    <div class="main-wrapper">
      <div class="section main">
        <div class="nav-bar">
          <img class="logo" href="#" alt="Witnet logo" />
          <div class="nav">
            <nav class="links">
              <ul>
                <li class="link">
                  <a href=""><span class="slash">/</span>oracle</a>
                </li>
                <li class="link">
                  <a href=""><span class="slash">/</span>token</a>
                </li>
                <li class="link">
                  <a href=""><span class="slash">/</span>ecosystem</a>
                </li>
                <li class="link">
                  <a href=""><span class="slash">/</span>community</a>
                </li>
                <li class="link">
                  <a href=""><span class="slash">/</span>blog</a>
                </li>
              </ul>
            </nav>
            <div class="language-selector">Language selector</div>
            <p class="github-icon">Github</p>
          </div>
        </div>
        <div class="left">
          <div class="title-wrapper">
            <h1 class="title">
              Unleash de power of smart contracts<span class="dot">.</span>
            </h1>
          </div>
          <p class="description">{{ $t('description') }}</p>
          <div class="buttons">
            <Button>>Build with Witnet</Button>
            <Button>> Start mining <span class="wit">wit</span></Button>
          </div>
        </div>

        <div class="right">
          <p>(nice illustration here)</p>
        </div>
      </div>
    </div>

    <div class="announcement">
      <div class="wrapper">
        <div class="announcement-content">
          <p class="tag">ANNOUNCEMENT</p>
          <h2 class="subtitle">Witnet is now side-chanined to Ethereum</h2>
        </div>
        <Button color="black">
          > Learn how to use Witnet from a solidity contract
        </Button>
      </div>
    </div>

    <div class="decentralized-oracle">
      <div class="wrapper">
        <div class="content">
          <div class="text">
            <h2 class="title">
              The decentralized oracle that is true to the censorship resistant
              nature of blockchains.
            </h2>
            <p class="paragraph">
              Without a reliable oracle, smart contracts can be vulnerable to
              hacks, corruption and monetary loss.
            </p>
            <p class="paragraph">
              Witnet leverages state-of-the-art cryptographic and economic
              techniques to provide your smart contracts with secure datainput.
            </p>
          </div>
          <div class="image">
            <p class="illustration">(Nice illustration here)</p>
          </div>
        </div>
        <Button color="black" class="margin-top">> Build with witnet</Button>
      </div>
    </div>

    <nuxt-content :document="page" />

    <div>testimonials</div>
    <div>wit token</div>
    <div>ecosystem</div>
    <div>Get involved</div>
    <div>Questions</div>
    <div>footer</div>
  </div>
</template>

<script>
import Button from '@/components/Button'

export default {
  components: {
    Button,
  },
  async asyncData({ app, params, $content }) {
    const { slug } = params
    const page = await $content(
      app.i18n.locale,
      'current_announcement',
      slug
    ).fetch()

    console.dir(page, { depth: null })

    return {
      page,
    }
  },
}
</script>

<style lang="scss">
// lightgreen = #5fbfae
// background =#12243a

.section {
  color: white;
  display: flex;
  align-items: center;
  width: 1280px;
  background: #12243a;
}

.main-wrapper {
  background: #12243a;
  display: flex;
  height: 100vh;
  width: 100%;
  justify-content: center;
}

.main {
  height: 100vh;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto 1fr;

  .nav-bar {
    height: 90px;
    grid-column: span 2;
    display: flex;
    width: 100%;

    .logo {
      width: 150px;
      height: auto;
    }
    .nav {
      align-items: center;
      display: flex;
      width: 100%;

      .links {
        & ul {
          display: flex;
        }

        .link {
          font-size: 18px;
          list-style: none;
          text-decoration: none;
          margin-right: 60px;
          & a {
            text-decoration: none;
            color: white;
          }
          .slash {
            color: #5fbfae;
          }
        }
      }
    }

    .language-selector {
      margin-right: 40px;
    }

    // .github-icon {}
  }

  .left {
    width: 500px;

    .title-wrapper {
      display: block;
      width: 100%;

      .title {
        font-size: 54px;
        font-weight: bold;
        // line-height: 50px;
        display: inline;
        color: #12243a;
        word-wrap: break-word;
        background: white;

        .dot {
          color: #5fbfae;
        }
      }

      margin-bottom: 48px;
    }

    .description {
      font-size: 20px;
      font-weight: bold;
      margin-bottom: 48px;
    }

    .buttons {
      .button {
        margin-right: 16px;
      }
    }
  }

  .right {
    width: 600px;
    height: 400px;
    border: 2px solid white;
    position: relative;
    z-index: 10;
    border-radius: 6px;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .right::after {
    content: '';
    display: block;
    position: absolute;
    z-index: -1;
    top: -25px;
    left: -25px;
    right: 15px;
    bottom: 15px;
    border: 2px solid #5fbfae;
    border-radius: 6px;
  }
}

.decentralized-oracle {
  display: flex;
  justify-content: center;

  .wrapper {
    display: flex;
    flex-direction: column;
    width: 1280px;

    .content {
      width: 100%;
      display: grid;
      grid-template-columns: 1fr 1fr;
      align-items: center;

      .text {
        max-width: 554px;

        .title {
          font-size: 40px;
          font-weight: bold;
          margin-bottom: 32px;
        }

        .paragraph {
          font-size: 18px;
          margin-bottom: 16px;
        }
      }
      .image {
        justify-self: center;
        .illustration {
          border-radius: 50%;
          background: #fff;
          width: 300px;
          height: 300px;
          align-items: center;
          display: flex;
          justify-content: center;
        }
      }
    }

    .margin-top {
      margin-top: 16px;
    }
  }
}
.announcement {
  height: 100px;
  background: #f9f9f9;
  display: flex;
  justify-content: center;

  .wrapper {
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    width: 1280px;
    .announcement-content {
      width: fit-content;
      .tag {
        font-size: 12px;
        color: #999;
        font-weight: bold;
      }
      .subtitle {
        font-size: 14px;
        font-size: 20px;
      }
    }

    .btn {
      justify-self: center;
    }
  }
}
</style>
