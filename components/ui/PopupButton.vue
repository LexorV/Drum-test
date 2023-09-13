<template>
  <button :style="cssVars" class="button" :type="type" @click="onClick">
    {{ text }}
  </button>
</template>

<script>
/// можно передать цвет кнопки пропсом
export default {
  props: {
    color: {
      type: String,
      default: 'inherit'
    },
    type: {
      type: String,
      default: 'button'
    },
    text: {
      type: String,
      default: 'OK'
    },
    onClick: {
      type: Function,
      default: () => {}
    }
  },
  computed: {
    cssVars () {
      return {
        '--color': this.color
      }
    }
  }
}
</script>

<style lang="css"  scoped>
  .button {
    width: 180px;
    height: 50px;
    background: var(--color);
    border-radius: 15px;
    border: none;
    @extend %text-big;
    color:  #FFFFFF;
    transition: all ease .5s;
    cursor: pointer;
;
  }
  button:active {
    transform: scale(.9);
}
@media screen and (max-width: calc(#{$tablet} - 120px)) {
  .button {
    width: 120px;
    height: 40px;
    font-size: 16px;
    line-height: 19px;
  }
}
</style>
