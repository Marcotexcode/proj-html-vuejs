<template>

  <div class="container">
    <div class="container--box">
      <h3 class="container--title">contact information</h3>
      <hr class="container--space">

      <p class="container--text">121 King Street, London United Kingdom</p>

      <span class="container--number">1.800.458.556</span>

      <div class="container--permiss">
        <p class="container--permiss--text">For privacy reasons Google Maps needs your permission to be loaded.</p>
        <button class="container--permiss--btn">i accept</button>
      </div>
    </div>
  </div>

</template>



<script>

export default {



}

</script>



<style scoped lang="scss">

  @import '@/style/variabili.scss';
  @import '@/style/mixins.scss';

  .container {
    width: calc(100% / 3);
    padding: 50px;

    .container--title{
      text-transform: uppercase;
      font-weight: 400;
    }

    .container--space {
      width: 15%;
      margin: 20px 0px;
      background: $Pelorous;
      height: 3px;
      border: none;
      border-radius: 20px;
    }
    
    .container--text {
      color: $Raven;
      margin: 20px 0px;
    }

    .container--number {
      color: $Raven;
    }

    .container--permiss {
      width: 100%;
      background-color: $FrenchGray;
      padding: 30px;
      text-align: center;
      margin-top: 30px;
    }

    .container--permiss--text {
      color: $Raven;
      line-height: 2;

    }

    .container--permiss--btn {
      @include btnPelorous();
      padding: 10px 30px;
    }
  }

</style>