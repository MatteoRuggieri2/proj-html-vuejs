<template>

    <!-- Percentage Cards -->
    <div class="percentage-card-container">

        <!-- Single Card -->
        <div v-for="(element, index) in percentages" :key="index" class="col-32">
            <div class="card-primary">
                                
                <div class="single-chart">
                    <svg viewBox="0 0 36 36" class="circular-chart primary-col">
                    <path class="circle-bg"
                        d="M18 2.0845
                        a 15.9155 15.9155 0 0 1 0 31.831
                        a 15.9155 15.9155 0 0 1 0 -31.831"
                    />
                    <path class="circle"
                        :stroke-dasharray="`${element.percentage}, 100`"
                        d="M18 2.0845
                        a 15.9155 15.9155 0 0 1 0 31.831
                        a 15.9155 15.9155 0 0 1 0 -31.831"
                    />
                    <text x="18" y="20.35" class="percentage">95%</text>
                    </svg>
                </div>

                <div class="percentage-name">{{ element.name }}</div>
            </div>
        </div>


    </div>


</template>

<script>
export default {
    name: 'PercentageCard',
    props: {
        percentages: Array,
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';

    .percentage-card-container {
        width: 60%;
        display: flex;
        justify-content: space-between;
        position: absolute;
        top: 75%;
        left: 50%;
        transform: translateX(-50%);
        z-index: 2;

        .card-primary {
            padding: 50px;

            .single-chart {
                width: 100%;
                justify-content: space-around ;
            }

            .circular-chart {
                display: block;
                margin: 10px auto;
                max-width: 100%;
                max-height: 250px;
            }

            .circle-bg {
                fill: none;
                stroke: #eee;
                stroke-width: 1.6;
            }

            .circle {
                fill: none;
                stroke-width: 1.6;
                stroke-linecap: round;
                animation: progress 1s ease-out forwards;
            }

            @keyframes progress {
                0% {
                    stroke-dasharray: 0 100;
                }
            }

            .circular-chart.primary-col .circle {
                stroke: $primary_color;
            }

            .percentage {
                fill: #666;
                font-family: sans-serif;
                font-size: 0.5em;
                text-anchor: middle;
            }
        }
    }

</style>