<template>
    <section class="portfolio-detail">
        <div class="container">
            <!-- full images -->
            <div class="full-img">
                <img src='https://i.ibb.co/N2yyBtK/aoi-full.jpg' alt="아오이 플라워">
            </div>
            <!-- portfolio details -->
            <div class="project-detail">
                <!-- 상세내용 -->
                <div class="contents">
                    <h4>project detail</h4>
                    <p>
                        플로리스트 아오이 플라워의 개인 홍보사이트를 제작하였습니다. <br>
                        개인의 이력 및 홍보를 위해 매번 PDF 파일로 어필을 했던 부분에 불편함을 느껴 사이트를 제작했고<br>
                        이력과 취급품목, 클래스 안내, SNS 등으로 구성하였습니다. <br>
                        PC 버전과 모바일 버전의 반응형으로 제작하였고 모든 이미지는 실제로 플로리스트분이 직접 만든 작품들입니다.<br>
                        배포 및 유지보수의 편의성을 위해 vue.js 기반의 Nuxt 프레임워크로 제작하였고 ,<br>
                        netlify 에 배포를 하였습니다. 
                    </p>
                </div>
                <!-- 스킬안내등 -->
                <div class="infos">
                    <ul>
                        <li>
                            <span>project</span>
                            <p>플로리스트 홍보사이트</p>
                        </li>
                        <li>
                            <span>position</span>
                            <p>웹디자인, 퍼블리싱</p>
                        </li>
                        <li>
                            <span>skills</span>
                            <p>HTML5, CSS3, VUE.JS</p>
                        </li>
                        <li>
                            <span>view code</span>
                            <p><a href='https://github.com/kimjihun-dev/floist_aoi_flower' class="github" target="_blank">github</a></p>
                        </li>
                        <li>
                            <span>view site</span>
                            <p><a href='https://aoiflower.netlify.app' class="demo" target="_blank">demo</a></p>
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
export default {
    head () {
        return {
            title: '플로리스트 아오이플라워'
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
    .back { margin-block: 55px; }
}

@media (max-width: 768px) {
    .infos { width: 90%; }
    .infos ul li:nth-child(3), .infos ul li:nth-child(4), .infos ul li:nth-child(5) { height: 0px; }
    .back { text-align: right; margin: 90px 0 50px; }
}

</style>