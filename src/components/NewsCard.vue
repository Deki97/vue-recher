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



/* -------------------------------------------- 
VERSIONE DESKTOP
-------------------------------------------- */
.col {
    padding: 0 20px;

    .single-news {
        
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
                    line-height: 1.5rem;
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
/* -------------------------------------------- 
VERSIONE DESKTOP 
-------------------------------------------- */





  /* -------------------------------------------- 
VERSIONE LARGE DEVICES (>768px && < 992px)
 -------------------------------------------- */
 @media (max-width: 992px) {
    .col {
        .single-news {
            .news-bottom {
                padding: 10px 0;

                .details {
                    position: absolute;
                    left: 0;
                    bottom: 0;
                }
            }
        }
    }
}
  /* -------------------------------------------- 
VERSIONE LARGE DEVICES (>768px && < 992px)
 -------------------------------------------- */



 @media (min-width: 769px) {
    .col {
        .single-news {
            min-height: 550px;
            .news-bottom {
                

                .text {
                    p {
                        
                    }
                }

                .details {
                    position: absolute;
                    left: 0;
                    bottom: 0;
                }
            }
        }
    }
}




@media (min-width: 993px) {
    .col {
        .single-news {
            min-height: 550px;
            .news-bottom {
                padding: 20px;

                .details {
                    position: absolute;
                    left: 20px;
                    bottom: 20px;
                }
            }
        }
    }
}





  /* -------------------------------------------- 
VERSIONE MEDIUM DEVICES (>576px && < 768px)
 -------------------------------------------- */
@media (max-width: 768px) {
    .col {
        .single-news {
            margin-bottom: 50px;
            .news-bottom {
                padding: 10px 0;

                .text {
                    p {
                        margin: 10px 0 40px 0;
                    }
                }

                .details {
                    position: unset;
                }
            }
        }
    }
}
 /* -------------------------------------------- 
FINE VERSIONE MEDIUM DEVICES (>576px && < 768px)
 -------------------------------------------- */





/* -------------------------------------------- 
VERSIONE SMALL DEVICES (< 576px)
 -------------------------------------------- */
@media (max-width: 576px) {
    .col {
        .single-news {
            .news-bottom {
                padding: 10px 0;
                .text {
                    p {
                        font-size: 1rem;
                        line-height: 1.3rem;
                    }
                }
            }
        }
    }
}
/* -------------------------------------------- 
FINE VERSIONE SMALL DEVICES (< 576px)
 -------------------------------------------- */
</style>