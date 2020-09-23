<template>
    <section class="portfolio">
        <div class="container">
            <div class="item-wrapper">
                <div class="card" v-for="item in portfolios" :key="item.id" :id="item.id">
                    <nuxt-link :to="'portfolio/' + item.id">
                        <img :src='item.thumbnail' alt="">
                        <div class="portfolio-overlay">
                            <div class="overlay-title">
                                <h3>{{ item.title }}</h3>
                            </div>
                        </div>
                    </nuxt-link>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import axios from 'axios'
export default {
    props: ['id'],
    data(){
        return {
            portfolios: [],
        }
    },
  async created () {
    const config = {
      headers: {
        Accept: 'application/json'
      }
    }
    try {
      const res = await axios.get('https://drf-portfolio-api.herokuapp.com/api/', config)
      this.portfolios = res.data
      console.log(this.portfolios)
    } catch (err) {
      console.log(err)
    }
  },
    head() {
        return {
            title: 'PORTFOLIO',
        }
    }
}
</script>

<style>
.item-wrapper { display: flex; flex-wrap: wrap; justify-content: space-between; transition: all 0.5s }
.card { position: relative; flex: 0 1 32%; height: 306px; margin-bottom: 2%; background: #ccc; transition: all 0.5s; }
.card img { max-width: 100%; width: 100%; height: 100%; }

.portfolio-overlay { position: absolute; background: #222; color: #ffffff; top: 0; left: 0; right: 0; bottom: 0; width: 100%; height: 100%; text-align: center; vertical-align: top; opacity: 0; transition: all 0.4s ease-in-out; }
.overlay-title { position: absolute; top: 50%; left: 50%;  -webkit-transform: translate(-50%, -50%); -ms-transform: translate(-50%, -50%); transform: translate(-50%, -50%); }
.overlay-title h3 { font-size: 18px; }
.card:hover .portfolio-overlay { opacity: 0.9; }

@media (max-width: 1024px) {
    .card { flex: 0 1 49%; }
}
@media (max-width: 767px) {
    .card { flex: 0 1 100%; margin-bottom: 3%; }
}

</style>
