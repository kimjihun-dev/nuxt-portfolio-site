<template>
    <section class="main">
        <div class="container">
            <div class="main-bg">
                <div class="welcome">
                    <p class="txt">kimjihun portfolio.</p>
                    <span>
                        포트폴리오들은 상업적인 아닌 개인 포트폴리용입니다.
                    </span>
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
.welcome .txt { font-size: 25px; margin-bottom: 10px; font-weight: bold; color: #fff; text-transform: uppercase;  }
.welcome span { font-size: 14px; color: #ddd; }
@media (max-width: 768px) {
    .welcome { padding-top: 0; transform: translateY(-0%); padding-left: 35px; }
    .welcome { padding-top: 50%; }
}
</style>
