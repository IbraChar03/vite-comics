<script >
import HeaderApp from './components/HeaderApp.vue'
import FirstMainApp from './components/FirstMainApp.vue'
import SecondMainApp from './components/SecondMainApp.vue'
import FirstFooterApp from './components/FirstFooterApp.vue'
import SecondFooterApp from './components/SecondFooterApp.vue'
export default {
  components: {
    HeaderApp,
    FirstMainApp,
    SecondMainApp,
    FirstFooterApp,
    SecondFooterApp
  }
}
</script>

<template>
  <header>
    <HeaderApp />
  </header>

  <main>
    <FirstMainApp />
    <SecondMainApp />
  </main>

  <footer>

    <FirstFooterApp />
    <SecondFooterApp />

  </footer>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
