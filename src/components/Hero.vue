<template>
  <div class="hero">
    <!-- Desktop -->
    <div class="d-none d-md-block">
      <div class="row mt-4">
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong>Best Game Menu, </strong> <br />
                in Your PC!
              </h2>
              <p>Ayo segera pilih dan beli game favorit Kamu</p>
              <router-link class="btn green light-1 btn-lg btn-success white--text " to="/games">
                <b-icon-cart ></b-icon-cart>Buy
              </router-link>
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <img src="../assets/images/Hero.png" width="100%" />
        </div>
      </div>
    </div>

    <!-- Mobile -->
    <div class="d-sm-block d-md-none">
      <div class="row mt-4">
        <div class="col-md-6 mb-3">
          <img src="../assets/images/Hero.png" width="100%" />
        </div>
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong>Best Game Menu, </strong> <br />
                in Your PC!
              </h2>
              <p>Ayo segera pilih dan beli game favorit Kamu</p>
              <button class="btn btn-lg btn-success">
                <b-icon-cart></b-icon-cart>Buy
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Hero",
};
</script>

<style>
</style>