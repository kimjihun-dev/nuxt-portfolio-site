<template>
    <section class="portfolio-detail">
        <div class="container">
            <!-- full images -->
            <div class="full-img">
                <img src='https://i.ibb.co/rpy9rXR/yeonje-ver2.jpg' alt="연제일신병원 리뉴얼 버전2">
            </div>
            <!-- portfolio details -->
            <div class="project-detail">
                <!-- 상세내용 -->
                <div class="contents">
                    <h4>project detail</h4>
                    <p>
                        개인 프로젝트로 진행했던 병원 사이트 리뉴얼을, 개선 작업을 하였습니다.<br>
                        전체적으로 컨텐츠들을 재배치하고 폰트크기라던가 반응형에서의 가독성 부분을 고려하여, <br>
                        디자인하였습니다. 피그마를 이용하여 디자인 작업 후 제플린을 이용하여, 퍼블리싱을 하였습니다.
                    </p>
                </div>
                <!-- 스킬안내등 -->
                <div class="infos">
                    <ul>
                        <li>
                            <span>project</span>
                            <p>병원사이트 리뉴얼 Ver2</p>
                        </li>
                        <li>
                            <span>position</span>
                            <p>웹디자인, 퍼블리싱</p>
                        </li>
                        <li>
                            <span>skills</span>
                            <p>html5, css3, javascript</p>
                        </li>
                        <li>
                            <span>view code</span>
                            <p><a href='https://github.com/kimjihun-dev/yeonje_re' class="github" target="_blank">github</a></p>
                        </li>
                        <li>
                            <span>view site</span>
                            <p><a href='https://kimjihun-dev.github.io/yeonje_re/' class="demo" target="_blank">demo</a></p>
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
            title: '연제일신병원 리뉴얼 ver2'
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