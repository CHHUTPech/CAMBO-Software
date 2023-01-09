<template>
  <div class="home-section">
    <div class="home-section-body container">
      <h3>
        Start And Manage Your Business With<br />
        <span>CAMBO Software</span>.
      </h3>
      <p>We start ~ We Growth ~ We Success</p>
      <GroupCard></GroupCard>
    </div>
  </div>
</template>

<style scoped>
.home-section {
  background-image: url("~assets/img/Home_Background.jpg");
  background-size: cover;
  padding: 2rem 0;
  display: flex;
  justify-content: center;
  color: white;
}
.home-section .home-section-body {
  padding: 2rem 0;
  /* outline: 1px solid red; */
}
.home-section .home-section-body > h3 {
  text-align: center;
  padding: 2rem 0;
  font-size: 3rem;
}
.home-section .home-section-body > h3 span {
  color: #cc8e1a;
}
.home-section .home-section-body > p {
  text-align: center;
  text-transform: uppercase;
}

@media only screen and (max-width: 48em) {
  .home-section .home-section-body > h3 {
    font-size: 1.7rem;
    padding: 1rem 0;
  }
}
</style>
