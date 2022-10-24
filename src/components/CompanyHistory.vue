<template>
    <div class="company-history d-flex flex-wrap">
        <div class="image">
            <img :src="image" :alt="title">
        </div>
        <div class="text d-flex flex-column align-items-center justify-content-between">
            <h2>{{ title }}</h2>

            <div class="btn-more">
                <a href="">{{ btnText }}</a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CompanyHistory',
    data: function() {
        return {
            image: require('../assets/img/history.png'),
            title: 'La nostra storia',
            btnText: 'Scopri di più'
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

.company-history {
    padding: 40px 0 120px 0;

    & > div {
        width: 50%;
    }

    .text {
        background-color: $page_secondary_color;
        color: white;
        padding: 120px 20px;

        h2 {
            text-transform: uppercase;
            font-size: 3.6rem;
            font-weight: 700;
        }

        .btn-more {
            a {
                color: white;
                font-size: 1.1rem;
                text-transform: uppercase;
                letter-spacing: -1px;
                border: 1px solid white;
                padding: 10px 20px;
                font-weight: 600;
            }
        }
    }
}

</style>