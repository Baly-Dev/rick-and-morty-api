<template>
  <div>
    <AppCharacters />
  </div>
</template>

<script>
import AppCharacters from "./components/AppCharacters.vue";

export default {
  name: 'App',
  components: {
    AppCharacters
}
}
</script>

<style lang="scss">
  
@import "./styles/global.scss";

</style>
