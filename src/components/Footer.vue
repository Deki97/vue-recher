<template>
    <footer class="text-center">
        <div class="container">
            <div class="footer-top">
                <div class="row">

                    <div class="col col1">
                        <div class="location">
                            <div>
                                {{ companyInfo.street }}
                            </div>
                            <div>
                                <span>{{ companyInfo.cap }}</span> 
                                <span> {{ companyInfo.place }} </span>
                                <span> {{ companyInfo.prov }} </span>
                                <span> {{ companyInfo.country }}</span>
                            </div>
                        </div>
                    </div>

                    <div class="col col2">
                        <div class="contacts">
                            <div>
                                Tel.{{ companyInfo.telephone }}
                            </div>
                            <div>
                                Email {{ companyInfo.mail }}
                            </div>
                        </div>
                    </div>

                    <div class="col col3">
                        <div>
                            Orario: {{ companyInfo.openHours }}
                        </div>
                    </div>
                    
                </div>
            </div>

            <div class="footer-bottom">
                <div class="row d-flex align-items-center">
                    
                    <div class="col col1">
                        <div class="logo">
                            <img :src="companyInfo.logo" :alt="companyInfo.name">
                        </div>
                    </div>

                    <div class="col col2">
                        <div class="company-name">
                            {{ companyInfo.name }}
                        </div>
                        <div>
                            C.F. e P.IVA {{ companyInfo.p_iva }}
                        </div>
                    </div>

                    <div class="col col3">
                        <div class="menu-footer">
                            <ul>
                                <li v-for="(menu, index) in menus" :key="index">
                                    <a :href="menu.url">{{ menu.name }}</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                    
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
    data: function() {
        return {
            closure: 'Web by www.bin8studios.com',
            companyInfo: {
                street: 'Via del Costo, 10',
                cap: '36010',
                place: 'Zanè',
                prov: '(VI)',
                country: 'Italia',
                telephone: '0445 372305',
                mail: 'info@studiolegalern.it',
                openHours: 'Lun - Ven / 09:00 - 13.00 / 15.00 - 19:00',
                logo: require('../assets/img/logo_footer.png'),
                name: 'Studio Legale Associato Recher & Nsundi',
                p_iva: '03533160242'
            },
            menus: [
                {
                    name: 'Homepage',
                    url: '#'
                },
                {
                    name: 'Lo Studio',
                    url: '#'
                },
                {
                    name: 'Contatti',
                    url: '#'
                },
                {
                    name: 'Informativa sui cookie',
                    url: '#'
                },
                {
                    name: 'Privacy',
                    url: '#'
                },
                {
                    name: 'Gestisci cookie',
                    url: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

footer {
    background-color: $page_secondary_color;
    padding: 80px 0;
    color: white;

    .footer-top {
        font-size: 1.1rem;
        font-weight: 700;
        .col {
            &.col2 {
                border-left: 1px solid white;
                border-right: 1px solid white;
            }
        }
    }

    .footer-bottom {
        margin-top: 80px;

        .logo {
            img {
                
            }
        }

        .col.col2 {
            & > .company-name {
                font-weight: 700;
            }
        }

        .menu-footer {
            ul li {
                a {
                    color: white;
                    font-size: 1.05rem;
                }
            }
        }
    }
}


</style>