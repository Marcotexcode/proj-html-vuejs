
<template>

  <div class="container">
    <div class="container--box">
      <h3 class="container--box--title">medical departments</h3>

      <hr class="container--box--space">

      <ul class="container--box--list">
        <li class="container--box--list--item"><i class="icon fas fa-check-circle"></i>Cardiology</li>
        <li class="container--box--list--item"><i class="icon fas fa-check-circle"></i>Pediatrics</li>
        <li class="container--box--list--item"><i class="icon fas fa-check-circle"></i>Diabetes Care</li>
        <li class="container--box--list--item"><i class="icon fas fa-check-circle"></i>Pre-natal Care</li>
        <li class="container--box--list--item"><i class="icon fas fa-check-circle"></i>Ultrasound Echocardiogram</li>
      </ul>

      <button class="container--box--btn">view our departments</button>
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
    padding: 20px;

    .container--box--title {
      text-transform: uppercase;
      font-weight: 400;
    }

    .container--box--space {
      width: 20%;
      margin: 20px 0px;
      background: $Pelorous;
      height: 3px;
      border: none;
      border-radius: 20px;
    }

    .container--box--list {
      list-style: none
    }

    .container--box--list--item {
      color: $Raven;
      margin: 10px;
      
    }

    .icon {
      font-size: 30px;
      color: $Pelorous;
      margin-right: 10px;
      vertical-align: middle;
    }


    .container--box--btn {
      @include btnPelorous();
      width: 100%;
      padding: 10px 30px;
    }
  }


</style>