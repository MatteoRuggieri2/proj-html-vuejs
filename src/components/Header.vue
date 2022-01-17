<template>
    <header>
        
        <!-- Header Top -->
        <div class="header-top">
            <div class="container">
                <div class="wrapper">
                    <span>We have a 95% Successful Pass Rate!</span>
                    <span>
                        <span>icon</span>
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
                                <a href="#">{{ element.name }}</a>
                            </li>
                        </ul>
                        <a class="btn btn-primary" href="#">book now</a>
                    </nav>
                
                </div>
            </div>
        </div>

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

        .header-top {
            padding: 10px 0;
            background-color: black;
            color: $secondary_color;
            font-size: 14px;

            .wrapper {
                display: flex;
                justify-content: space-between;
            }
        }

        .header-bottom {
            padding: 30px 0;
            background-color: rgba(0, 0, 0, 0.5);
            color: $secondary_color;
            
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
                        }
                    }

                    .btn {
                        margin-left: 20px;
                    }
                }
            }
        }
    }
</style>