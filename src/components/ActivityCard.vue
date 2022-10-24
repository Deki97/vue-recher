<template>
    <div class="col">
        <div class="single-activity">
            <div class="activity-image">
                <img :src="activityObject.image" :alt="activityObject.name">

                <div class="activity-name">
                    <h4>{{ activityObject.name }}</h4>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ActivityCard',
    props: {
        activityObject: Object
    },

}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

.single-activity {
    height: 380px;
    border-radius: 10px;

    .activity-image {
        width: 100%;
        height: 100%;
        position: relative;
        border-radius: 10px;
        

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 10px;
        }

        .activity-name {
            position: absolute;
            bottom: -14%;
            left: 50%;
            transform: translateX(-50%);
            background-color: #fff;
            width: 90%;
            min-height: 120px;
            text-align: center;
            border-radius: 10px;
            border-bottom: 3px solid $page_secondary_color;
            padding: 10px 20px;

            h4 {
                text-transform: uppercase;
                margin-top: 10px;
                font-size: 1.2rem;
                font-weight: 600;
            }
        }
    }
}

</style>