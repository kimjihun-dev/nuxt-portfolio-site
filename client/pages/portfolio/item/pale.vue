<template>
    <section class="portfolio-detail">
        <div class="container">
            <!-- full images -->
            <div class="full-img">
                <img src='https://i.ibb.co/HT68Y0v/pale-full.jpg' alt="">
            </div>
            <!-- portfolio details -->
            <div class="project-detail">
                <!-- 상세내용 -->
                <div class="contents">
                    <h4>project detail</h4>
                    <p>부산 해운대구 소재 호텔사이트를 리뉴얼 하였습니다.<br>
                    예약 및 방을 검색 할 수 있는 폼을 중앙에 배치하였으며 datapicker library 를 이용하여, <br>
                    체크인 및 체크아웃의 날짜를 선택시 몇박인지 알려주게끔 구현하였습니다.<br>
                    호텔의 이벤트 및 소개, sns 순서대로 컨텐츠들을 배치하였습니다.</p>
                </div>
                <!-- 스킬안내등 -->
                <div class="infos">
                    <ul>
                        <li>
                            <span>project</span>
                            <p>팔레드시즈 호텔사이트 리뉴얼</p>
                        </li>
                        <li>
                            <span>position</span>
                            <p>웹디자인, 퍼블리싱</p>
                        </li>
                        <li>
                            <span>skills</span>
                            <p>HTML5, CSS3, jQuery</p>
                        </li>
                        <li>
                            <span>view code</span>
                            <p><a href='https://github.com/kimjihun-dev/pale_de_cz' class="github" target="_blank">github</a></p>
                        </li>
                        <li>
                            <span>view site</span>
                            <p><a href='https://kimjihun-dev.github.io/pale_de_cz' class="demo" target="_blank">demo</a></p>
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
            title: '팔레드시즈 리뉴얼'
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