<template>
  <div class="navbar">
    <div class="navbar-body">
      <div class="logo">
        <nuxt-link to="/">
          <img src="~/assets/img/navbarlogo.svg" alt="logo" />
        </nuxt-link>
      </div>
      <div class="menu" :class="{ show: isShow }">
        <img src="~/assets/img/navbarlogo.svg" alt="logo" />
        <div class="menu-body" v-for="data in navbarmenu" :key="data.id">
          <nuxt-link :to="data.url"
            ><p style="text-transform: uppercase">{{ data.text }}</p></nuxt-link
          >
        </div>
        <div class="btn-contact">
          <button @click="test">Contact Us</button>
        </div>
      </div>
      <div class="btn-close-open">
        <div v-if="isShow" @click="test">
          <svg width="32" height="32" viewBox="0 0 1024 1024">
            <path
              fill="currentColor"
              d="M195.2 195.2a64 64 0 0 1 90.496 0L512 421.504L738.304 195.2a64 64 0 0 1 90.496 90.496L602.496 512L828.8 738.304a64 64 0 0 1-90.496 90.496L512 602.496L285.696 828.8a64 64 0 0 1-90.496-90.496L421.504 512L195.2 285.696a64 64 0 0 1 0-90.496z"
            />
          </svg>
        </div>
        <div class="btn-menu" v-if="!isShow" @click="test">
          <p>Menu</p>
          <svg width="25" height="25" viewBox="0 0 24 24">
            <path
              fill="currentColor"
              d="M4 6h16v2H4zm0 5h16v2H4zm0 5h16v2H4z"
            />
          </svg>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    isShow: false,
  }),
  computed: {
    navbarmenu() {
      return this.$store.state.navbarmenu.list
    },
  },
  methods: {
    test() {
      this.isShow = !this.isShow
    },
  },
}
</script>

<style scoped>
.navbar {
  display: flex;
  justify-content: center;
  align-items: center;
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 50;
  padding: 0.5rem;
  background: white;
  box-shadow: 0px 4px 8px 0px rgba(0, 0, 0, 0.1);
  -webkit-box-shadow: 0px 4px 8px 0px rgba(0, 0, 0, 0.1);
  -moz-box-shadow: 0px 4px 8px 0px rgba(0, 0, 0, 0.1);
}
.navbar .navbar-body {
  display: flex;
  align-items: center;
  top: 0;
  justify-content: space-between;
  max-width: 1366px;
  width: 100%;
}
.navbar .navbar-body .logo a > img {
  width: 200px;
  object-fit: contain;
  object-position: center;
}
.navbar .navbar-body .btn-close-open {
  color: #000063;
  cursor: pointer;
}
.navbar .navbar-body .btn-close-open .btn-menu p {
  font-weight: 700;
  /* font-size: 1.5rem; */
}

.navbar .navbar-body .menu {
  display: flex;
  align-items: center;
}
.navbar .navbar-body .menu img {
  display: none;
}
.navbar .navbar-body .menu .menu-body {
  display: flex;
}

.navbar .navbar-body .menu .menu-body a {
  text-decoration: none;
  padding: 0 1rem;
  font-weight: 600;
  color: #000063;
  transition: all 0.3s;
}
.navbar .navbar-body .menu .menu-body a:hover {
  color: #cc8e1a;
}
.navbar .navbar-body .btn-contact {
  display: flex;
  align-items: center;
}
.navbar .navbar-body .btn-close-open {
  display: none;
}
.navbar .navbar-body .btn-contact > button {
  border: 2px solid #a37214;
  background: #a37214;
  padding: 0.5rem 1rem;
  color: #000063;
  color: white;
  cursor: pointer;
  font-weight: 700;
  border-radius: 0.2rem;
}
.navbar .navbar-body .btn-contact > button:hover {
  border: 2px solid #8a5f11;
  background: #8a5f11;
}

/* responsive */

@media only screen and (max-width: 85em) {
  .navbar .navbar-body {
    padding: 0 6rem;
  }
}
@media only screen and (max-width: 64em) {
  .navbar .navbar-body {
    padding: 0 3rem;
  }
}
@media only screen and (max-width: 48em) {
  .navbar .navbar-body {
    padding: 0 1rem;
    
  }
  .navbar .navbar-body .menu {
    /* background: #000063; */
    background: white;
    position: absolute;
    flex-direction: column;
    text-align: start;
    box-shadow: 5px 0px 7px 0px rgba(0, 0, 0, 0.37);
    -webkit-box-shadow: 5px 0px 7px 0px rgba(0, 0, 0, 0.37);
    -moz-box-shadow: 5px 0px 7px 0px rgba(0, 0, 0, 0.37);
    top: 0;
    left: -300vh;
    align-items: flex-start;
    transition: all 0.3s;
    padding-left: 2rem;
  }
  .navbar .navbar-body .menu .menu-body a {
    padding: 0.5rem 0;
  }
  .navbar .navbar-body .show {
    left: 0;
    top: 0;
    transition: all 0.3s;
  }
  .navbar .navbar-body .btn-close-open {
    display: flex;
  }
  .navbar .navbar-body .btn-close-open .btn-menu {
    display: flex;
    align-items: center;
  }

  .navbar .navbar-body .menu {
    display: flex;
    width: 70%;
    padding-bottom: 2rem;
    height: 100vh;
    justify-content: center;
  }
  .navbar .navbar-body .menu .menu-body {
    flex-direction: column;
    align-items: center;
  }
  .navbar .navbar-body .menu img {
    display: flex;
    width: 200px;
    position: absolute;
    top: 3rem;
    left: 2rem;
  }
  .navbar .navbar-body .menu .btn-contact {
    padding-top: 2rem;
  }
}
</style>
