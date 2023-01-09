<template>
  <div class="group-card">
    <div class="group-card-body">
      <Card name="POS System" />
      <Card name="Buy Product from China" />
      <Card name="Stock Management System" />
    </div>
  </div>
</template>

<style scoped>
.group-card {
  display: flex;
  justify-content: center;
  text-align: center;
}
.group-card .group-card-body {
  display: grid;
  padding: 2rem;
  grid-template-columns: repeat(3, 1fr);
}
@media screen and (max-width: 64em) {
  .group-card .group-card-body {
    grid-template-columns: repeat(2, 1fr);
  }
}
@media screen and (max-width: 48em) {
  .group-card .group-card-body {
    grid-template-columns: repeat(1, 1fr);
  }
}
</style>
