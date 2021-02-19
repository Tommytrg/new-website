<template>
  <div>
    <div class="main-wrapper">
      <div class="section main">
        <div class="nav-wrapper">
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
            <h1 class="title">Unleash de power of smart contracts.</h1>
          </div>
          <p>
            Witnet enables your smart contract to react to real world events
            with strong crypto-economic guarantees
          </p>
          <button>> Build with Witnet</button>
          <button>> Start mining <span class="wit">wit</span></button>
        </div>
        <div class="right"></div>
      </div>
    </div>

    <div>Announcement</div>

    <div>The decentralized oracle</div>

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
.section {
  display: flex;
  align-items: center;
  width: 1280px;
  background: lightcyan;
}

.main-wrapper {
  background: darkblue;
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

  .nav-wrapper {
    grid-column: span 2;
    display: flex;

    .logo {
      width: 150px;
      height: auto;
    }
    .nav {
      display: flex;
      width: 100%;
      justify-content: flex-end;
      .links {
        & ul {
          display: flex;
        }

        .link {
          color: black;
          list-style: none;
          text-decoration: none;
          margin-right: 40px;
          & a {
            text-decoration: none;
          }
          .slash {
            color: green;
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
    .title-wrapper {
      display: block;
      width: 100%;
      .title {
        font-size: 40px;
        font-weight: 600;
        line-height: 50px;
        display: inline;
        background: burlywood;
        color: darkcyan;
        padding: 2px;
        word-wrap: break-word;
        width: 100%;
      }
    }
  }
}
</style>
