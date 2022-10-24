<template>
    <div class="col">
        <div class="single-news">
            <div class="news-top">
                <div class="image">
                    <img :src="newsObject.image" :alt="newsObject.title">
                </div>
            </div>
            <div class="news-bottom">
                <div class="title">
                    <h3>{{ newsObject.title }}</h3>
                </div>
                <div class="text">
                    <p>{{ newsObject.text }}</p>
                </div>

                <div class="details">
                    <div class="date">
                        {{ newsObject.date }}
                    </div>
                    <div class="btn-more">
                        <a :href="newsObject.newsUrl">
                            {{ newsObject.btnText }}
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'NewsCard',
    props: {
        newsObject: Object
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

.col {
    padding: 0 20px;

    .single-news {
        min-height: 500px;
        position: relative;
        .news-top {
            height: 200px;

            .image {
                width: 100%;
                height: 100%;

                img {
                    width: 100%;
                    height: 100%;
                    object-fit: cover;
                }
            }
        }

        .news-bottom {
            padding: 20px;

            .title {
                h3 {
                    font-size: 1.6rem;
                }
            }

            .text {
                p {
                    font-size: 1.2rem;
                    margin: 20px 0;
                }
            }

            .details {
                position: absolute;
                left: 20px;
                bottom: 20px;

                .date
                {
                    margin: 10px 0;
                }

                .btn-more {
                    margin-top: 20px;

                    a {
                        color: black;
                        font-size: 1.1rem;
                        font-weight: 700;
                    }
                }
            }
        }
    }
}

</style>