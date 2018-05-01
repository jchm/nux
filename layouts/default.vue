<template>
  <div class="app">
    <header class="app-header">
      <app-logo/>
      <app-navigation/>
    </header>
    <main class="app-main">
        <nuxt/>
    </main>
  </div>
</template>
<script>
import AppLogo from '~/components/AppLogo.vue'
import AppNavigation from '~/components/AppNavigation.vue'

export default {
  components: {
    AppLogo,
    AppNavigation
  }
}
</script>

<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: border-box;
  margin: 0;
}

.app {
   display: grid;
   grid-template-rows: minmax(auto, 100px);
}

.app-header {
    border-bottom: solid 1px  #eee;
    box-shadow: 0 0 3px #eee;
    background-color: #fff;

    display: flex;
    align-items: center;
    padding: 1em;

    position: sticky;
    top: 0;
}
</style>
