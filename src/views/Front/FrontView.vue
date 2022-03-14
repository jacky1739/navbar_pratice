<template>
  <section class="section">
    <div class="container">
      <h3 class="title">Our Games</h3>
      <h4 class="subtitle">Amiga games are made for quality entertainment.
        <br>
        We strive to be on the top of the crowd's gaming experience.
      </h4>
    </div>
    <div class="container card">
      <div class="card">
        <div class="card__wrapper">
          <a href="#">
            <img src="../../assets/images/3000-90b0a485.png" alt="">
          </a>
        </div>
      </div>
      <div class="card">
        <div class="card__wrapper">
          <a href="#">
            <img src="../../assets/images/3000-90b0a485.png" alt="">
          </a>
        </div>
      </div>
      <div class="card">
        <div class="card__wrapper">
          <a href="#">
            <img src="../../assets/images/3000-90b0a485.png" alt="">
          </a>
        </div>
      </div>
      <div class="card">
        <div class="card__wrapper">
          <a href="#">
            <img src="../../assets/images/3000-90b0a485.png" alt="">
          </a>
        </div>
      </div>
      <div class="card">
        <div class="card__wrapper">
          <a href="#">
            <img src="../../assets/images/3000-90b0a485.png" alt="">
          </a>
        </div>
      </div>
      <div class="card">
        <div class="card__wrapper">
          <a href="#">
            <img src="../../assets/images/3000-90b0a485.png" alt="">
          </a>
        </div>
      </div>
      <div class="card">
        <div class="card__wrapper">
          <a href="#">
            <img src="../../assets/images/3000-90b0a485.png" alt="">
          </a>
        </div>
      </div>
      <div class="card">
        <div class="card__wrapper">
          <a href="#">
            <img src="../../assets/images/3000-90b0a485.png" alt="">
          </a>
        </div>
      </div>
      <div class="card">
        <div class="card__wrapper">
          <a href="#">
            <img src="../../assets/images/3000-90b0a485.png" alt="">
          </a>
        </div>
      </div>
      <div class="card">
        <div class="card__wrapper">
          <a href="#">
            <img src="../../assets/images/3000-90b0a485.png" alt="">
          </a>
        </div>
      </div>
      <div class="card">
        <div class="card__wrapper">
          <a href="#">
            <img src="../../assets/images/3000-90b0a485.png" alt="">
          </a>
        </div>
      </div>
      <div class="card">
        <div class="card__wrapper">
          <a href="#">
            <img src="../../assets/images/3000-90b0a485.png" alt="">
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  .section {
    padding-top: .48rem;
    background-image: url('../../assets/images/background16-3-1920x1263-c36d62b2.jpg');
    height: 100vh;
    width: 100%;
  }
  .title {
    font-weight: bold;
    font-size: 0.82rem;
    line-height: 1.2;
    letter-spacing: 1;
    text-align: center;
    @media (max-width: 768px) {
      font-size: calc( .32rem + ( .82 - .32 ) * (( 100vw - .24rem ) / (12 - .24)));
      line-height: calc( 1.4 * (.27rem + (4.6 - 2.26) * (( 100vw - 2rem) / (48 - 20))));
    }
  }
  .subtitle {
    margin-bottom: .2rem;
    text-align: center;
    font-size: .142rem;
    line-height: 1.6;
    margin-bottom: .5rem;
  }
  .card {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    margin-bottom: .3rem;
  }
  .card__wrapper {
    width: 2.08rem;
    height: 1.59rem;
    margin: 0 .16rem;
    @media (max-width: 1200px) {
      width: 2.18rem;
    }
    @media (max-width: 992px) {
      width: 2.08rem;
    }
  }
</style>

<script>
export default {
  data () {
    return {
      data: []
    }
  }
}
</script>
