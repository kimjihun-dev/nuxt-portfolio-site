<template>
    <header class="page-header">
        <h1 class="page-brand">
            <nuxt-link to="/portfolio">
            Portfolio.
            </nuxt-link>
        </h1>
        <nav class="page-nav">
            <ul class="page-nav-list">
                <li class="page-nav-item" v-for="(link, index) in navLinks" :key="index">
                    <nuxt-link :to='link.route' exact>
                        {{ link.text }}
                    </nuxt-link>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            navLinks: [
                { route: '/portfolio', text: 'Portfolio' },
                { route: '/about', text: 'About', },
            ]
        }
    },
}
</script>

<style>
header { max-width: 1100px; width: 100%; margin: 0 auto; }
.page-header { display: flex; justify-content: space-between; align-items: center; height: 90px; padding-top: 2%; }
.page-brand { margin: 0 10px; font-size: 1.9rem; font-weight: bold; letter-spacing: -2px; }
.page-nav-list { display: flex; margin: 0; padding: 0; list-style: none; }
.page-nav-item { margin: 0 10px; }
.page-nav-item a { text-decoration: none; color: #333; }
.page-nav-item a.nuxt-link-active { color: crimson; }

@media (max-width: 1024px) {
    header { padding: 0 3%; }
}
@media (max-width: 768px) {
    header { padding: 0 2%; }
}
</style>