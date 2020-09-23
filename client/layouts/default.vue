<template>
  <div id="wrap">
    <AppHeader />    
    <Nuxt />
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from '../components/AppHeader'
import AppFooter from '../components/AppFooter'

export default {
    components: {
        AppHeader,
        AppFooter,
    },
}
</script>

<style>
* { margin: 0; padding: 0; box-sizing: border-box; }
body { font-family: 'NanumSquare', sans-serif; font-size: 14px; color: #333; }
a { text-decoration: none; color: inherit;  }
ul { list-style: none; }
.container { max-width: 1100px; width: 100%; margin: 0 auto; padding-top: 2%; }
.nuxt-link-active { font-weight: bold; }
.nuxt-link-exact-active { font-weight: bold; }

@media (max-width: 1024px) {
    .container { padding: 0 3%; }
}
@media (max-width: 768px) {
    .container { padding: 0 2%; }
}
</style>
