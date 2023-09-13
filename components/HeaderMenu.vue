<template>
  <header>
    <ul>
      <li>
        <PopupButton />
        <p>тест</p>
      </li>
    </ul>

  </header>
</template>

<script lang="ts">
import PopupButton from '@/components/ui/PopupButton.vue'
export default {
  components: {
    PopupButton
  },
  name: 'headerMenu',
}
</script>

<style scoped>
.header {
  display: flex;

}

.menu {
  display: flex;
  justify-content: center;
  width: 100%;
}

.heading {
  margin: 0;
  width: 100%;
}

@media screen and (max-width: 450px) {
  .heading {
    font-size: 16px;
  }
}
</style>
