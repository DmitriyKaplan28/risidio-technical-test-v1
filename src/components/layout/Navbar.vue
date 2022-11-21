<template>

  <div class="nav-bar">
    <div class="navbar_container">
      <img class="nav_banner"
           src="https://res.cloudinary.com/risidio/image/upload/v1633609222/RisidioMarketplace/gradienta-m_-1_v4hs5p.svg"
           alt="">
    </div>

    <div class="main-navbar">

      <div class="residio-logo-container">
        <img class="logo" :src="logo" alt="risidio-logo"/>
        <img
            class="toggle"
            :src="isActive ? require('../../assets/close_menu.svg') : require('../../assets/burger_menu.svg')"
            @click="openMenu">
      </div>

      <div :class="isActive ? 'menu is-active' : 'menu'">
        <li class="nav-item"> Gallery</li>
        <li class="nav-item"> Featured Collections</li>

        <div class="border"></div>

        <li class="nav-item right"> How It Works</li>
        <li class="nav-item"> about Risidio</li>
        <li class="nav-nft-item">My NFTs</li>

        <button>Register with Hiro Wallet</button>

      </div>
    </div>
  </div>

</template>

<script>

export default {
  data() {
    return {
      logo: 'https://res.cloudinary.com/risidio/image/upload/v1633609248/RisidioMarketplace/Group_-1_fgpanq.svg',
      isActive: false,
    }
  },
  methods: {
    openMenu() {
      return this.isActive = !this.isActive
    }
  }
}

</script>


<style scoped>

.toggle {
  display: none;
  width: 25px;
  height: 22px;
  cursor: pointer;
}

.main-navbar {
  padding: 15px 50px 20px 50px;
  display: flex;
  flex-direction: row;
  align-items: center;
}

.menu {
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
}

.menu button {
  display: none;
}

.nav-item {
  list-style-type: none;
  margin: 0 20px;
  color: white;
  font-size: 12px;
  line-height: 15px;
  cursor: pointer;
}

.right {
  margin-left: auto;
}

.nav_banner {
  position: absolute;
  top: 0;
  width: 100%;
  height: 100px;
  object-fit: cover;
  z-index: -11;
}

.nav-nft-item {
  width: 133px;
  height: 43px;
  background: rgba(255, 255, 255, 0.2);
  border-radius: 22px;
  display: flex;
  justify-content: center;
  align-items: center;
  font: normal normal bold 12px/15px Montserrat;
  color: #5FBDC1;
}

.border {
  display: none;
}


@media (max-width: 428px) {
  .main-navbar {
    padding: 0;
    flex-direction: column;
  }

  .residio-logo-container {
    padding: 13px 20px;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-image: url("../../assets/background.svg");
    z-index: 20;
  }

  .right {
    margin-left: 20px;
  }

  .border {
    display: block;
    margin: 30px 20px 30px 20px;
    height: 1px;
    width: 80%;
    background-color: lightgray;
    opacity: 0.2;
  }

  .toggle {
    display: block;
  }

  .main-navbar button {
    background: rgba(80, 177, 181, 0.2);
    border-radius: 22px;
    font: normal normal bold 11px/14px Montserrat;
    color: #5FBDC1;
    width: 90%;
    margin-top: 60px;
    height: 43px;
    border: none;
  }

  .logo {
    width: 97px;
    height: 44px;
  }

  .nav_banner {
    height: 70px;
  }

  .menu {
    position: absolute;
    top: 70px;
    display: none;
    flex-direction: column;
    align-items: flex-start;
    padding: 20px 20px 20px 20px;
    gap: 20px;
    width: 100%;
    z-index: 20;
    background-image: url("../../assets/background.svg");
  }

  .menu.is-active {
    display: flex;
  }

  .menu img {
    display: none;
  }

  .menu button {
    display: block;
  }
}

</style>