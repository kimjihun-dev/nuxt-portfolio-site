<template>
    <section class="portfolio-detail">
        <div class="container">
            <!-- full images -->
            <div class="full-img">
                <img src='https://i.ibb.co/SQH7TMw/portfolio-full.jpg' alt="포트폴리오 사이트">
            </div>
            <!-- portfolio details -->
            <div class="project-detail">
                <!-- 상세내용 -->
                <div class="contents">
                    <h4>project detail</h4>
                    <p>
                        포트폴리오 사이트를 구축하였습니다.<br>
                        VUE 기반 NUXT.JS 프레임워크로 제작을 하였으며 정적 웹사이트 호스팅 서비스인 <br>
                        netlify 에 배포를 하였습니다. 단순 html 페이지들로만 구성된 기존의 사이트들 보며 <br>
                        포트폴리오들을 관리,배포하기 편한 방법을 찾다가 개인프로젝트 겸 제작 하였으며, <br>
                        Header, Footer 등의 반복적으로 사용 되는 부분은 컴포넌트로 제작, 프레임워크에서 제공되는 <br>
                        파일만 만들어도 자동으로 만들어주는 라우팅 기능으로 포트폴리오 페이지들을 구축하였습니다. 
                    </p>
                </div>
                <!-- 스킬안내등 -->
                <div class="infos">
                    <ul>
                        <li>
                            <span>project</span>
                            <p>포트폴리오 사이트 구축</p>
                        </li>
                        <li>
                            <span>position</span>
                            <p>웹디자인, 퍼블리싱, 프로그래밍</p>
                        </li>
                        <li>
                            <span>skills</span>
                            <p>HTML5, CSS3, NUXT.JS</p>
                        </li>
                        <li>
                            <span>view code</span>
                            <p><a href='https://github.com/kimjihun-dev/nuxt-portfolio-site' class="github" target="_blank">github</a></p>
                        </li>
                        <li>
                            <span>view site</span>
                            <p><a href='https://kimjihun-portfolio.netlify.app/portfolio' class="demo" target="_blank">demo</a></p>
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
            title: '포트폴리오 사이트 구축'
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