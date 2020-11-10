<template>
    <section class="portfolio-detail">
        <div class="container">
            <!-- full images -->
            <div class="full-img">
                <img src='https://i.ibb.co/jRbznV9/some-full.jpg' alt="닭썸">
            </div>
            <!-- portfolio details -->
            <div class="project-detail">
                <!-- 상세내용 -->
                <div class="contents">
                    <h4>project detail</h4>
                    <p>
                        부산 신평동에서 영업하고 있는 닭썸 신평점 홍보용 전단지 디자인을 하였습니다. <br>
                        식욕을 돋구는 레드색상을 배경색으로 넣었으며 실제 고객들에게 제공되는 <br>
                        음식들을 촬영하여 전단지내에 배치하였습니다. 해당 매장의 사장님의 의중을 최우선으로 하여 작업하였습니다. <br>
                        일러스트로 작업을 하였으며 인쇄용 A4 사이즈로 제작 후 출력작업을 진행하였습니다. 
                    </p>
                </div>
                <!-- 스킬안내등 -->
                <div class="infos">
                    <ul>
                        <li>
                            <span>project</span>
                            <p>닭썸 전단지 디자인</p>
                        </li>
                        <li>
                            <span>position</span>
                            <p>편집디자인</p>
                        </li>
                        <li>
                            <span>skills</span>
                            <p>포토샵, 일러스트</p>
                        </li>
                        <!-- <li>
                            <span>view code</span>
                            <p><a href='https://github.com/kimjihun-dev/assembly' class="github" target="_blank">github</a></p>
                        </li>
                        -->
                        <li>
                            <span>view site</span>
                            <p><a href='https://www.instagram.com/p/CFKLxJlsQLb/' class="demo" target="_blank">View</a></p>
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
            title: '닭썸 신평점 전단지 디자인'
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