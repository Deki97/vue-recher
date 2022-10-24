<template>
    <div class="wrapper">
        <div class="activities">
            <h2>{{ title }}</h2>
            <div class="row row-cols-1 row-cols-md-2 row-cols-xl-4">
                <ActivityCard v-for="(activity, index) in activities"
                :key="index" 
                :activityObject="activity" /> 
            </div>  
        </div>
    </div>
</template>

<script>
import ActivityCard from './ActivityCard.vue'

export default {
    name: 'Activities',
    components: {
        ActivityCard
    },
    data: function() {
        return {
            title: 'Le nostre attività',
            activities: [
                {
                    name: 'Imprese e società',
                    image: require('../assets/img/activity1.png')
                },
                {
                    name: 'Diritto del lavoro',
                    image: require('../assets/img/activity2.png')
                },
                {
                    name: 'Insolvenza e crisi d\'impresa e del consumatore',
                    image: require('../assets/img/activity3.png')
                },
                {
                    name: 'Responsabilità civile',
                    image: require('../assets/img/activity4.png')
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

.activities {
    margin: 100px 0 140px 0;

    h2 {
        text-align: center;
        text-transform: uppercase;
        font-weight: 400;
        margin-bottom: 40px;
    }
}

</style>