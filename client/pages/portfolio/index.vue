<template>
    <section class="portfolio">
        <div class="container">
            <div class="item-wrapper">
                <!-- card -->
                <div class="card" v-for="(item, index) in pData" :key="index">
                    <nuxt-link :to=item.route>
                        <img :src='item.thum' alt="">
                        <div class="portfolio-overlay">
                            <div class="overlay-title">
                                <h3>{{ item.title }}</h3>
                            </div>
                        </div>
                    </nuxt-link>
                </div>
                <!-- end card -->
            </div>
        </div>
    </section>
</template>

<script>
export default {

    data() {
        return {
            pData: [
                
                { route: 'portfolio/item/yeonje_ver2', title: '연제일신병원 리뉴얼 VER2', thum: 'https://i.ibb.co/rbDxWg1/yeonje-ver2-thum.jpg' },
                { route: 'portfolio/item/aoiflower', title: '플로리스트 홍보사이트', thum: 'https://i.ibb.co/TWT12Tk/aoi-thum.jpg' },
                { route: 'portfolio/item/some/', title: '닭썸 전단지 작업', thum: 'https://i.ibb.co/1GQjXwW/chicken.jpg' },
                { route: 'portfolio/item/siteBuild/', title: '포트폴리오 사이트 구축', thum: 'https://i.ibb.co/tJZ3gQh/portfolio-thum.jpg' },
                { route: 'portfolio/item/nts/', title: '부산지방국세청 리뉴얼', thum: 'https://i.ibb.co/7WV2JNH/item08.jpg' },
                { route: 'portfolio/item/tong/', title: '동명대학교 리뉴얼', thum: 'https://i.ibb.co/MVFHH4k/item01.jpg' },
                { route: 'portfolio/item/codinote/', title: '코디노트 퍼블리싱', thum: 'https://i.ibb.co/X5mLhrJ/codinote-thum.jpg' },
                { route: 'portfolio/item/assm/', title: '국회사이트 리뉴얼', thum: 'https://i.ibb.co/Wvdv3tt/assm-thum.jpg' },
                { route: 'portfolio/item/museum/', title: '부산 복천박물관 리뉴얼', thum: 'https://i.ibb.co/6XMfcVf/museum-thum.jpg' },
                { route: 'portfolio/item/yeonje/', title: '연제일신병원 리뉴얼', thum: 'https://i.ibb.co/q0gQyzV/yeonje-thum.jpg' },
                { route: 'portfolio/item/pale/', title: '팔레드시즈 리뉴얼', thum: 'https://i.ibb.co/41t57ws/pale-thum.jpg' },
            ]
        }
    },

    head() {
        return {
            title: '김지훈 포트폴리오',
        }
    }
}
</script>

<style>
.item-wrapper { display: flex; flex-wrap: wrap; justify-content: space-between; transition: all 0.5s }
.card { position: relative; flex: 0 1 32%; height: 306px; margin-bottom: 2%; background: #ccc; transition: all 0.5s; }
.card img { max-width: 100%; width: 100%; height: 100%; }

.portfolio-overlay { position: absolute; background: #222; color: #ffffff; top: 0; left: 0; right: 0; bottom: 0; width: 100%; height: 100%; text-align: center; vertical-align: top; opacity: 0; transition: all 0.4s ease-in-out; }
.overlay-title { position: absolute; top: 50%; left: 50%;  -webkit-transform: translate(-50%, -50%); -ms-transform: translate(-50%, -50%); transform: translate(-50%, -50%); }
.overlay-title h3 { font-size: 18px; }
.card:hover .portfolio-overlay { opacity: 0.9; }

@media (max-width: 1024px) {
    .card { flex: 0 1 49%; }
}
@media (max-width: 767px) {
    .card { flex: 0 1 100%; margin-bottom: 5%; }
    .item-wrapper { padding: 0 3%; }
}

</style>
