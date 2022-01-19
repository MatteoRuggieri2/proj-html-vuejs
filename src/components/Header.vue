<template>
    <header>
        
        <!-- Header Top -->
        <div class="header-top">
            <div class="container">
                <div class="wrapper">
                    <span>We have a 95% Successful Pass Rate!</span>
                    <span>
                        <span class="phone-icon"><i class="fas fa-phone"></i></span>
                        <span>Give us a call to book your tuition! 1-800-555-555</span>
                    </span>
                </div>
            </div>
        </div>

        <!-- Header Bottom -->
        <div class="header-bottom">
            <div class="container">
                <div class="wrapper">
                    
                    <!-- Logo -->
                    <div class="logo">
                        <img src="../assets/img/avada-drivers-logo-2x.png" alt="Logo Avada Drivers">
                    </div>

                    <!-- Nav -->
                    <nav>
                        <ul>
                            <li v-for="(element, index) in headerLinks" :key="index">
                                <a :class="element.active ? 'active' : false" href="#">
                                    {{ element.name }}
                                </a>
                                <span v-if="element.new" class="new-tag">new</span>
                            </li>
                        </ul>
                        <a class="btn btn-primary" href="#">book now</a>
                    </nav>
                
                </div>
            </div>
        </div>

        <span class="sales-tags">
            <span class="single-tag">
                <div class="wallet-icon"><i class="fas fa-window-maximize"></i></div>
                <span>Demos</span>
            </span>
            <span class="single-tag">
                <div class="discounted-price">
                    <span class="dollar">$</span>
                    <span class="price">39</span>
                </div>
                <span>On Sale</span>
            </span>
        </span>

    </header>
</template>

<script>
export default {
    name: 'Header',
    props: {
        headerLinks: Array
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';

    header {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;

        .header-top {
            padding: 10px 0;
            background-color: #353637;
            color: $primary_text_color;
            font-size: 12px;

            .wrapper {
                display: flex;
                justify-content: space-between;

                .phone-icon {
                    margin-right: 15px;
                }
            }
        }

        .header-bottom {
            padding: 30px 0;
            background-color: #35363788;   // Prendere il colore principale dell'header e schiarirlo
            color: $secondary_color;
            font-size: 14px;
            font-weight: bold;
            
            .wrapper {
                display: flex;
                justify-content: space-between;
                align-items: center;

                .logo {
                    width: 230px;
                    flex-shrink: 0;
                }

                nav {
                    display: flex;
                    text-transform: uppercase;

                    ul {
                        display: flex;
                        align-items: center;

                        li {
                            margin: 0 20px;

                            a {
                                padding-bottom: 5px;
                                &.active {
                                    color: $primary_color;
                                    border-bottom: 2px solid $primary_color;
                                }

                                &:hover {
                                    color: $primary_color;
                                }
                            }

                            .new-tag {
                                background-color: $primary_color;
                                font-size: 10px;
                                padding: 2px 4px;
                                border-radius: 4px;
                            }
                        }
                    }

                    .btn {
                        margin-left: 20px;
                    }
                }
            }
        }

        .sales-tags {
            display: inline-block;
            display: flex;
            flex-direction: column;
            position: fixed;
            top: 120px;
            right: 0;
            z-index: 20;

            .single-tag {
                display: inline-block;
                width: 65px;
                height: 65px;
                margin: 5px 10px;
                padding: 10px;
                background-color: white;
                font-size: 11px;
                font-weight: 600;
                border-radius: 7px;
                color: #33475b;
                display: flex;
                flex-direction: column;
                justify-content: space-between;
                align-items: center;

                // test
                border: 1px solid black;

                .wallet-icon {
                    font-size: 20px;
                    color: #33475b;
                }

                .discounted-price {
                    color: $primary_color;

                    .dollar {
                        font-size: 16px;
                        vertical-align: top;
                    }

                    .price {
                        font-size: 24px;
                    }
                }
            }
        }
    }
</style>