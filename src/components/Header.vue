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


            <!-- <nav class="navbar navbar-expand-lg navbar-light d-flex justify-content-between">
                <a class="navbar-brand" href="#">
                    <img src="../assets/img/logo.png" alt="Recher Logo">
                </a>
                <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
                    <div class="navbar-nav">
                    <a class="nav-item nav-link active" href="#">Home</a>
                    <a class="nav-item nav-link" href="#">Features</a>
                    <a class="nav-item nav-link" href="#">Pricing</a>
                    </div>
                </div>
            </nav> -->
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