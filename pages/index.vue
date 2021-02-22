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
          <p class="description">
            Witnet enables your smart contract to react to real world events
            with strong crypto-economic guarantees.
          </p>
          <div class="buttons">
            <button class="button">> Build with Witnet</button>
            <button class="button">
              > Start mining <span class="wit">wit</span>
            </button>
          </div>
        </div>

        <div class="right">
          <p>(nice illustration here)</p>
        </div>
      </div>
    </div>

    <div class="announcement">
      <div class="content">
        <p class="tag">ANNOUNCEMENT</p>
        <h2 class="subtitle">Witnet is now side-chanined to Ethereum</h2>
      </div>
      <button class="button btn">
        > Learn how to use Witnet from a solidity contract
      </button>
    </div>

    <div>

    </div>

    <div>testimonials</div>
    <div>wit token</div>
    <div>ecosystem</div>
    <div>Get involved</div>
    <div>Questions</div>
    <div>footer</div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss">
// lightgreen = #5fbfae
// background =#12243a

.button {
  background: transparent;
  font-size: 18px;
  color: white;
  border-radius: 5px;
  padding: 16px;
  border: 2px solid white;
  outline: 0;
  text-decoration: none;
  cursor: pointer;
  white-space: nowrap;
  font-weight: bold;
  width: fit-content;
  height: fit-content;
  box-sizing: border-box;

  &:hover {
    color: #5fbfae;
    border-color: #5fbfae;
  }

  &:active {
    color: #468d80;
    border-color: #468d80;
  }
}

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

    .logo {
      width: 150px;
      height: auto;
    }
    .nav {
      align-items: center;
      display: flex;
      width: 100%;
      justify-content: flex-end;

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
      padding-left: 16px;
      margin-bottom: 48px;
    }

    .buttons {
      text-align: center;

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

.announcement {
  height: 100px;
  background: #f9f9f9;
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  justify-items: center;
  .content {
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
    border-color: black;
    color: black;
  }
}
</style>
