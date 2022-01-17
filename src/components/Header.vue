<template>
    <header>
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
    </header>
</template>

<script>
export default {
    name: 'Header',

// ricordati di fare i data con le props per header e footer
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';

    header {

        .header-top {
            padding: 10px 0;
            background-color: black;
            color: white;
            font-size: 14px;

            .wrapper {
                display: flex;
                justify-content: space-between;
            }
        }
    }
</style>