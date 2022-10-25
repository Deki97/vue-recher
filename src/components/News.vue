<template>
    <div class="container">
        <div class="news-container">
            <h2>{{ title }}</h2>
            <div class="row row-cols-1 row-cols-md-3">
                <NewsCard v-for="(news, index) in newsList" 
                :key="index" 
                :newsObject="news" />
                </div>
        </div>
    </div>
</template>

<script>
import NewsCard from './NewsCard.vue'

export default {
    name: 'News',
    components: {
        NewsCard
    },
    data: function() {
        return {
            title: 'News',
            newsList: [
                {
                    image: require('../assets/img/news1.png'),
                    title: 'Il nuovo sito web dello studio è online',
                    text: 'Siamo anche on line, con un\'area news presto aggiornata. Tornate a visitarci.',
                    date: '26 Set 2022',
                    btnText: 'Leggi di più',
                    newsUrl: '#'
                },
                {
                    image: require('../assets/img/news2.png'),
                    title: 'Lo studio vince un\'altra causa',
                    text: 'Lo studio si aggiudica la vittoria in una causa di responsabilità civile',
                    date: '14 Set 2022',
                    btnText: 'Leggi di più',
                    newsUrl: '#'
                },
                {
                    image: require('../assets/img/news3.png'),
                    title: 'Lorem ipsum dolor sit amet',
                    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas iaculis, felis ut suscipit dignissim, magna arcu elementum turpis.',
                    date: '18 Ago 2022',
                    btnText: 'Leggi di più',
                    newsUrl: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.news-container {
    margin: 100px 0;
    
    h2 {
        text-align: center;
        text-transform: uppercase;
        font-weight: 400;
        margin-bottom: 40px;
    }
}
</style>