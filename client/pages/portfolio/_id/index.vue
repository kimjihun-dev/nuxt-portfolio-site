<template>
    <section class="portfolio-detail">
        <div class="container">
            <!-- full images -->
            <div class="full-img">
                <img :src='portfolio.contentImg' alt="">
            </div>
            <!-- portfolio details -->
            <div class="project-detail">
                <!-- 상세내용 -->
                <div class="contents">
                    <h4>project detail</h4>
                    <p>{{ portfolio.content | safe }}</p>
                </div>
                <!-- 스킬안내등 -->
                <div class="infos">
                    <ul>
                        <li>
                            <span>project</span>
                            <p>{{ portfolio.title }}</p>
                        </li>
                        <li>
                            <span>position</span>
                            <p>{{ portfolio.position }}</p>
                        </li>
                        <li>
                            <span>skills</span>
                            <p>{{ portfolio.skills }}</p>
                        </li>
                        <li>
                            <span>view code</span>
                            <p><a :href=portfolio.code_view class="github" target="_blank">github</a></p>
                        </li>
                        <li>
                            <span>view site</span>
                            <p><a :href=portfolio.site_view class="demo" target="_blank">demo</a></p>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="back">
                <nuxt-link :to="'/portfolio'">BACK</nuxt-link>
            </div>
        </div>
    </section>
</template>

<script>
import axios from 'axios'
export default {
    data(){
        return {
            portfolio: {},
        }
    },

    async created () {
    const config = {
      headers: {
        Accept: 'application/json'
      }
    }
    try {
        const res = await axios.get(`https://drf-portfolio-api.herokuapp.com/api/${this.$route.params.id}`, config)
        this.portfolio = res.data
        console.log(this.portfolio)
        } catch (err) {
        console.log(err)
        }
    },
    head () {
        return {
            title: this.portfolio.title
        }
    }
}
</script>

<style>
.full-img img { max-width: 100%; width: 100%; height: auto; }
.project-detail { margin-top: 5%; display: flex; justify-content: space-between; text-transform: uppercase; }
.contents { width: 70%; margin-right: 3%; transition: all 0.5s; }
.contents h4 { font-size: 18px; color: #555; margin-bottom: 20px; }
.contents h4::after { content: ""; width: 100%; height: 1px; background: #ddd; display: inline-block; }
.contents p { line-height: 1.7; }
.infos { width: 30%; transition: all 0.5s; }
.infos ul li { margin: 15px 0; }
.infos ul li span { display: inline-block; color: #666; width: 130px; letter-spacing: 2px; font-size: 13px;  }
.infos ul li p {  display: inline-block; }
.github, .demo { color: rgb(48, 92, 238); font-weight: 500; text-decoration: underline; text-transform: none; }
.back { text-align: center; margin-top: 5%; }
.back a { border: 1px solid #000; padding: 13px; font-weight: normal; font-size: 15px; color: #fff; background: #333; }
.back a::after { display: inline-block; content: ""; width: 27px; height: 6px; background: url('~assets/images/arrow-btn.png') no-repeat; margin-left: 5px; }


@media (max-width: 1024px) {
    .project-detail { display: flex; flex-direction: column; }
    .contents { width: 100%; margin-right: 0%; margin-bottom: 3%; }
    .infos { width: 100%; }
}

@media (max-width: 768px) {
    .back { text-align: right; }
}

</style>