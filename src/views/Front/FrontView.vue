<template>
  <section class="section">
    <div class="container">
      <h3 class="title">Our Games</h3>
      <h4 class="subtitle">Amiga games are made for quality entertainment.
        <br>
        We strive to be on the top of the crowd's gaming experience.
      </h4>
    </div>
    <div class="card">
      <a href="#"><img src="" alt=""></a>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  .section {
    padding-top: .48rem;
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
