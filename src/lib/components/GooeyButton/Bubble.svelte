<script lang="ts">
    let min = -50;
    let max = -350;
    
</script>
<span class="absolute top-0 left-0 bg-green-500 rounded-full block z-[-1]"></span>
<style lang="scss">
    /* Bubbles Animation */
    // span:nth-child(1) {
    //     width: 25px;
    //     height: 25px;
    //     left: calc(10px);
    //     animation: move 3.2s infinite;
    //     animation-delay: 0.2s;
    // }
    // @keyframes move {
    // 0% {
    //     transform: translate(0, 0);
    // }
    // 99% {
    //     transform: translate(0, -430px);
    // }
    // 100% {
    //     transform: translate(0, 0);
    //     opacity: 0;
    // }
    // }
    // Define the animation name and duration

    span:nth-child(1) {
        width: 25px;
        height: 25px;
        left: calc(10px);
        animation: move 3.2s infinite;
        animation-delay: 0.2s;
    }
    
    $random: random(200);

    @keyframes move {

        0% {
        transform: translate(0, 0);
        }

        95% {
        transform: translate(0, $random - 250 + px);
        }

        100% {
        transform: translate(0, 0);
        opacity: 0;
        }
    }

</style>