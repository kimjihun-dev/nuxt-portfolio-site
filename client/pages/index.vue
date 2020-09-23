<template>
    <section class="main">
        <div class="container">
            <div class="main-bg"></div>
        </div>
  </section>
</template>

<script>
export default {
    head() {
        return {
            title: '김지훈 포트폴리오',
        }
    }
}
</script>

<style>
.main-bg { max-width: 100%; width: 100%; height: 550px; background: url('~assets/images/main-bg.jpg') no-repeat center/cover; }
@media (max-width: 767px) {
}
</style>
