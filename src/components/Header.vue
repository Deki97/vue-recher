<template>
    <header>
        <div class="container">
            <div class="header-wrapper d-flex align-items-center justify-content-between">
                <div class="header-left">
                    <div class="logo">
                        <img src="../assets/img/logo.png" alt="Recher Logo">
                    </div>
                </div>
                <div class="header-right">
                    <div class="menu">
                        <nav>
                            <ul class="d-flex">
                                <li v-for="(menu, index) in menus" :key="index">
                                    <a :href="menu.menuUrl">{{ menu.menuName }}</a>
                                </li>
                            </ul>
                        </nav>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data: function() {
        return {
            menus: [
                {
                    menuName: 'Homepage',
                    menuUrl: '#'
                },
                {
                    menuName: 'Lo Studio',
                    menuUrl: '#'
                },
                {
                    menuName: 'Le attività',
                    menuUrl: '#'
                },
                {
                    menuName: 'Dove siamo',
                    menuUrl: '#'
                },
                {
                    menuName: 'Contatti',
                    menuUrl: '#'
                },
                {
                    menuName: 'News',
                    menuUrl: '#'
                },
            ],

        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

header {
    padding: 20px 0;

    .header-right {
        .menu {
            nav {
                ul {
                    li {
                        margin-left: 24px;
                        font-size: 1.25rem;
                        text-transform: uppercase;
                        font-weight: 600;

                        a {
                            color: $page_primary_color;
                        }
                    }
                }
            }
        }
    }
}
</style>