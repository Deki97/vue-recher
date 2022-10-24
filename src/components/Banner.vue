<template>
    <div class="banner">
        <div class="image-banner">
            <img :src="banners[0].image" :alt="banners[0].bannerTitle">

            <div class="overlay"></div>

            <div class="text-content">
                <div class="banner-title">
                    <h2>{{ banners[0].bannerTitle }}</h2>
                </div>
                <div class="banner-subtitle">
                    <h4>{{ banners[0].bannerSubtitle }}</h4>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Banner',
    data: function() {
        return {
            banners: [
                {
                    image: require('../assets/img/banner1.png'),
                    bannerTitle: 'Il nostro team',
                    bannerSubtitle: 'Competenza e disponibilità a servizio del Cliente'
                },
                {
                    image: require('../assets/img/banner2.png'),
                    bannerTitle: 'Con il cliente, per il cliente',
                    bannerSubtitle: 'La nostra esperienza è la soluzione per ogni tuo problema e la risposta per le tue esigenze'
                },
                {
                    image: require('../assets/img/banner3.png'),
                    bannerTitle: 'La nostra sede',
                    bannerSubtitle: 'Palazzo delle Professioni 3^ Piano - Zanè (VI), via del Costo, n.10'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.banner {
    height: calc(100vh - 130px);

    .image-banner {
        width: 100%;
        height: 100%;
        position: relative;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.2);
        }

        .text-content {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: white;
            text-align: center;

            .banner-title {
                h2 {
                    font-size: 4rem;
                    letter-spacing: -1px;
                    text-transform: uppercase;
                }
            }

            .banner-subtitle {
                h4 {
                    font-size: 2.2rem;
                }
            }
        }
    }
}
</style>