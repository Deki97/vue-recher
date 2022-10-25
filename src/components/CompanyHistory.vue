<template>
    <div class="company-history d-flex flex-wrap">
        <div class="image">
            <img :src="image" :alt="title">
        </div>
        <div class="text d-flex flex-column align-items-center justify-content-center">
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

    & > div {
        width: 50%;
    }

    .text {
        background-color: $page_secondary_color;
        color: white;

        h2 {
            text-transform: uppercase;
            font-size: 2.6rem;
            font-weight: 700;
            margin-bottom: 60px;
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


// RESPONSIVE
@media (max-width: 1200px) {
    .company-history {
    
        .text {
            h2 {
                font-size: 1.8rem;
            }
 
        }
    }
}


@media (max-width: 768px) {
    .company-history {
        & > div {
            width: 100%;
        }
        .text {
            padding: 30px 0;

            h2 {
                font-size: 1.6rem;
            }

            .btn-more {
            a {
                font-size: 1.1rem;
                padding: 8px 15px;
            }
        }
        }
    }
}

@media (max-width: 576px) {
    .company-history {
        .text {
            padding: 30px 0;

            h2 {
                font-size: 1.2rem;
            }

            .btn-more {
            a {
                font-size: .9rem;
                padding: 8px 15px;
            }
        }
        }
    }
}



</style>