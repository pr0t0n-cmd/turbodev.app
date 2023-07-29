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
        <h1 class:light={mode === "light"}>
            TURBODEV.APP
        </h1>
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
        font-size: 3rem;
        margin-bottom: 1rem;
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
        animation: heartbeat 2s infinite;
    }

    @keyframes heartbeat {
    0%, 100% {
        transform: translateX(-50%) translateY(-105%) scale(1);
    }
    50% {
        transform: translateX(-50%) translateY(-105%) scale(0.8);
    }
    
    }
    .engine{
        position: relative;
    }
</style>