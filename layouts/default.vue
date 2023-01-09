<template>
  <div>
    <NavBar></NavBar>

    <main>
      <Nuxt />
    </main>
    <i class="fa-solid fa-house"></i>
    <Footer></Footer>
  </div>
</template>

<style scoped>
main {
  position: relative;
  top: 3rem;
  z-index: 0;
}
</style>
