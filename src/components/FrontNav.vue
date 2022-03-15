<template>
  <nav class="nav">
    <div class="container">
      <input type="checkbox" id="check">
      <label for="check" class="checkbtn">
        <span class="material-icons">
          reorder
        </span>
      </label>
      <label class="logo">DesignX</label>
      <ul class="list__group">
        <li class="list__group__item"><a class="list__group__link" href="#" @click.prevent="clickOn">Home</a></li>
        <li class="list__group__item"><a class="list__group__link" href="#">About</a></li>
        <li class="list__group__item"><a class="list__group__link" href="#">Serivces</a></li>
        <li class="list__group__item"><a class="list__group__link" href="#">Contact</a></li>
        <li class="list__group__item"><a class="list__group__link" href="#">Feedback</a></li>
      </ul>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
  .container {
    padding: 0 .3rem;
  }
  .nav {
    background: black;
    height: .8rem;
    width: 100%;
    .checkbtn {
      font-size: .3rem;
      color: white;
      float: right;
      line-height: .8rem;
      // margin-right: .4rem;
      cursor: pointer;
      display: none;
      @media (max-width: 858px) {
        display: block;
      }
    }
    #check {
      display: none;
    }
    #check:checked ~ ul {
      left: 0;
    }
    .logo {
      color: white;
      font-size: .35rem;
      line-height: .8rem;
      padding: 0 0 0 0;
      font-weight: bold;
      @media (max-width: 952px) {
        font-size: .3rem;
        // padding-left: .5rem;
      }
    }
    .list__group {
      float: right;
      // margin-right: .2rem;
      @media (max-width: 858px) {
        position: fixed;
        width: 100%;
        height: calc(100vh - .8rem);
        background: #2c3e50;
        top: .8rem;
        left: -100%;
        text-align: center;
        transition: all .5s;
      }
      &__item {
        display: inline-block;
        line-height: .8rem;
        margin: 0 .05rem;
        @media (max-width: 858px) {
          display: block;
          margin: .5rem 0;
          line-height: .3rem;
        }
      }
      &__link {
        color: white;
        font-size: .17rem;
        text-transform: uppercase;
        padding: .07rem .13rem;
        border-radius: .25rem;
        @media (max-width: 952px) {
          font-size: .16rem;
        }
        @media (max-width: 858px) {
          font-size: .2rem;
          .list__group__link.active, .list__group__link:hover {
            background: none;
            color: #0082e6;
          }
        }
      }
      .list__group__link.active, .list__group__link:hover {
        background: #1b9bff;
        transition: .5s;
      }
    }
  }
</style>

<script>
import emitter from '@/assets/javascript/emitter'

export default {
  methods: {
    clickOn () {
      console.log('click children layer')
      emitter.emit('click')
    }
  }
}
</script>
