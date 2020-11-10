<template>
    <section class="main">
        <div class="container">
            <div class="main-bg">
                <div class="welcome">
                    <p class="txt">kimjihun portfolio.</p>
                    <a href="/portfolio" class="btnA">view site</a>
                </div>
            </div>
        </div>
  </section>
</template>

<script>
export default {
    head() {
        return {
            title: '포트폴리오 메인',
        }
    }
}
</script>

<style>
.main-bg { max-width: 100%; width: 100%; height: 550px; background: url('~assets/images/main-bg.jpg') no-repeat center/cover; }
.welcome { padding-top: 50%; transform: translateY(-30%); padding-left: 35px; }
.welcome .txt { font-size: 25px; margin-bottom: 20px; font-weight: bold; color: #fff; text-transform: uppercase;  }
.welcome .btnA { color: rgb(206, 206, 206); font-size: 14px; text-transform: uppercase; position: relative; }
.welcome .btnA::after { position: absolute; content: ""; width: 27px; top: 5px; right: -33px; height: 6px; background: url('~assets/images/arrow-btn.png') no-repeat; }
@media (max-width: 768px) {
    .welcome { padding-top: 0; transform: translateY(-0%); padding-left: 35px; }
    .welcome { padding-top: 70%; }
}
</style>
