<template>
    <div class="pre-footer">
        <div class="container">
            <div class="pre-footer-content text-center">
                <div class="title">
                    <h3>{{ title }}</h3>
                </div>  
                <div class="text">
                    <p>{{ text }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'PreFooter',
    data: function() {
        return {
            title: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas iaculis, felis ut suscipit dignissim, magna arcu elementum turpis.',
            text: 'eneo domizio ulpiano'
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

.pre-footer {
    background-color: $page_tertiary_color;
    padding: 50px 0;

    &-content {
        .title {
            h3 {
                text-transform: uppercase;
                font-weight: 700;
                margin-bottom: 40px;
                font-size: 1.8rem;
            }
        }

        .text {
            p {
                font-size: 1.4rem;
            }
        }
    }
}

</style>