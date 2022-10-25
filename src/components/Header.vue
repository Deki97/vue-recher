<template>
    <header>
        <div class="container">
            <div class="header-wrapper d-flex align-items-center justify-content-between">
                <div class="header-left">
                    <div class="logo">
                        <img src="../assets/img/logo.png" alt="Recher Logo">
                    </div>
                </div>
                <div class="header-right-desktop d-none d-lg-block">
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

                <div class="header-right-mobile d-block d-lg-none">
                    <div @click="isHidden = !isHidden" class="burger-toggle">
                        <img src="../assets/img/menu.png" alt="Burger Toggle">
                    </div>

                    <div v-if="!isHidden" class="menu">
                        <nav>
                            <ul class="d-flex flex-column">
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
            isHidden: true,
            menus: [
                {
                    menuName: 'Homepage',
                    menuUrl: '/'
                },
                {
                    menuName: 'Lo Studio',
                    menuUrl: 'lo-studio'
                },
                {
                    menuName: 'Le attività',
                    menuUrl: '/le-attività'
                },
                {
                    menuName: 'Dove siamo',
                    menuUrl: '/dove-siamo'
                },
                {
                    menuName: 'Contatti',
                    menuUrl: '/contatti'
                },
                {
                    menuName: 'News',
                    menuUrl: '/news'
                },
            ],

        }
    },
    methods: {
        sayHello: function() {
            alert('Ciao');
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

header {
    padding: 20px 0;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 999;
    background-color: #fff;

    .header-left {
        .logo {
            img {
                width: 150px;
            }
        }
    }

    .header-right-desktop {
        .menu {
            nav {
                ul {
                    li {
                        margin-left: 24px;
                        font-size: .9rem;
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

    .header-right-mobile {
        .burger-toggle {
            img {
                width: 35px;
            }
        }

        .menu {
            position: absolute;
            top: 115px;
            right: 40px;
            background-color: white;
            width: 300px;
            border-radius: 5px;
            text-align: center;

            nav {
                ul {
                    li {
                        font-size: 1.2rem;

                        a {
                            color: black;
                            margin: 10px 0;
                            display: inline-block;
                            width: 100%;
                            height: 100%;
                        }
                    }
                }
            }
        }
    }
}


// RESPONSIVE
@media (min-width: 768px) {
header {
    .header-left {
        .logo {
            img {
                width: 200px;
            }
        }
    }

    .header-right-mobile {
        .burger-toggle {
            img {
                width: 40px;
            }
        }
    }
}
}



@media (min-width: 992px) {
header {
    .header-left {
        .logo {
            img {
                width: 250px;
            }
        }
    }
}
}



@media (min-width: 1200px) {
header {
        padding: 20px 0;

        .header-right-desktop {
            .menu {
                nav {
                    ul {
                        li {
                            margin-left: 24px;
                            font-size: 1.25rem;
                            text-transform: uppercase;
                            font-weight: 600;

                        
                        }
                    }
                }
            }
        }
    }
}


@media (max-width: 400px) {
    header {
        .header-right-mobile {
            .menu {
                right: 20px;
                width: 80%;
            }
        }
    }
}
</style>