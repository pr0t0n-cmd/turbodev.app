<script>
	import Logo from "$lib/components/Logo.svelte";
    let mode = "dark";
    let light = "#000";
    let dark = "#fff";
    const toggleMode = () => {
        switch (mode) {
            case 'dark':
                mode = "light";
                break;
            case 'light':
                mode = "dark";
                break;
        }
    }
</script>
<div class="content" class:contentLight={mode === "light"}>
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <!-- svelte-ignore a11y-no-static-element-interactions -->
    <div class="container" on:click={toggleMode}>
        <div class="engine">
            <!-- <img src={engine} alt="" width="520" height="520"> -->
            <div class="logo">
                <Logo fill={ mode === "light" ? light : dark }/>
            </div>
            <div class="orb"></div>
        </div>
        
        <h1 class="turbodev-app" class:light={mode === "light"}>
            <span>T</span>
            <span>U</span>
            <span>R</span>
            <span>B</span>
            <span>O</span>
            <span>D</span>
            <span>E</span>
            <span>V</span>
            <span>.</span>
            <span>A</span>
            <span>P</span>
            <span>P</span>
        </h1>
        <h2 class="font-bold underline text-white">Loading...</h2>
        <p class:light={mode === "light"}>
            web, e-commerce, mobile
        </p>
    </div>
</div>


<style>
    h1,
    p {
        color: #fff;
        text-align: center;
        text-shadow: 0px 0px 2px rgba(0, 0, 0, 0.05),
    }

    .light{
        color: #000 !important;
    }

    h1 {
        font-size: 2.75rem;
    }
    p {
        font-size: 1.75rem;
    }
    /* img{
        width: 300px;
        height: auto;
    } */
    .content {
        cursor: pointer;
        background-color: #000;
        width: 100vw;
        height: 100vh;
        display: flex;
        align-items: center;
        justify-content: center;
        padding: .5rem;
    }
    .contentLight{
        background-color: #fff !important;
    }
    .container{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    .orb{
        position: absolute;
        top: 50%;
        left: 50%;
        width: 55px;
        height: 55px;
        border-radius: 50%;
        background-color: #fff;
        box-shadow: 0 0 40px 20px #fff, 0 0 100px 50px rgba(0, 255, 94, 0.75);
        transform: translateX(-50%) translateY(-105%);
        animation: heartbeat 1s infinite;
    }

    @keyframes heartbeat {
    0%, 100% {
        transform: translateX(-50%) translateY(-105%) scale(1);
    }
    50% {
        transform: translateX(-50%) translateY(-105%) scale(0.5);
    }
    
    }
    .engine{
        position: relative;
    }

    .turbodev-app span {
        transform: translateY(-10px);
        margin: 0;
        display: inline-block;
        opacity: 0;
        animation: slideDown .75s forwards;
        letter-spacing: -10px;
    }
    @keyframes slideDown {
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }
    .turbodev-app span:nth-child(1) { animation-delay: calc(0.1s * 9); }
    .turbodev-app span:nth-child(2) { animation-delay: calc(0.1s * 10); }
    .turbodev-app span:nth-child(3) { animation-delay: calc(0.1s * 11); }
    .turbodev-app span:nth-child(4) { animation-delay: calc(0.1s * 12); }
    .turbodev-app span:nth-child(5) { animation-delay: calc(0.1s * 13); }
    .turbodev-app span:nth-child(6) { animation-delay: calc(0.1s * 14); }
    .turbodev-app span:nth-child(7) { animation-delay: calc(0.1s * 15); }
    .turbodev-app span:nth-child(8) { animation-delay: calc(0.1s * 16); }
    .turbodev-app span:nth-child(9) { animation-delay: calc(0.1s * 17); }
    .turbodev-app span:nth-child(10) { animation-delay: calc(0.1s * 18); }
    .turbodev-app span:nth-child(11) { animation-delay: calc(0.1s * 19); }
    .turbodev-app span:nth-child(12) { animation-delay: calc(0.1s * 20); }
</style>