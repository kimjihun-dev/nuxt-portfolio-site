<template>
    <section class="about">
        <div class="container about-inner">
            <div class="about-title">
                <h4>about</h4>
            </div>
            <div class="about-content">
                <p>
                    안녕하세요. 포트폴리오 사이트를 방문해주셔서 감사합니다.<br>
                    새로운 것을 배우는거에 두려움 없이<br>노력하고 공부하는 자세로 임하고 있습니다.
                </p>
            </div>
            <div class="about-intro">
                <p>1983년생</p>
                <p>010-2697-4836</p>
                <p>zodlab@kakao.com</p>
            </div>
            <a href="https://github.com/kimjihun-dev" class="github" target="_blank">
                <img src="~assets/images/github.png" alt="깃허브 아이콘" title="깃허브">
            </a>
        </div>
    </section>    
</template>

<script>
export default {
    head() {
        return {
            title: 'about ',
        }
    }
}
</script>

<style>
.about { height: 65vh; }
.about-inner { text-align: center; }
.about-title { position: relative; margin-top: 50px; }
.about-title h4 { font-size: 23px; font-weight: 900; color: #555; text-transform: uppercase; display: block;  }
.about-title h4::after { position: absolute; left: 50%; bottom: -5%; transform: translateX(-50%); content: ""; display: block; background: #555; width: 80px; height: 1px; }
.about-content { margin-top: 5%; line-height: 1.8; }
.about-intro { margin-top: 2%; }
.about-intro p { margin-bottom: 5px; }
.github { display: block; margin-top: 3%; }
.github img { width: 30px; }

@media (max-width: 767px) {
    .about-title { margin-top: 150px; }
    .about-content { margin-top: 7%; margin-bottom: 20px; }
    .github { margin-top: 50px; }
}
</style>