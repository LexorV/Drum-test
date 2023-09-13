<template>
  <div>
    <NuxtWelcome />
  </div>
</template>
<script>
  export default {
    mounted() {
      console.log(this.$store.state.count);
    },
  };
</script>
