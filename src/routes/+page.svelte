<script>
	import Logo from "$lib/components/Logo.svelte";
    let engine = "/img/engine.png"
</script>
<div class="content">
    <div>
        <div class="engine">
            <!-- <img src={engine} alt="" width="520" height="520"> -->
            <div class="logo">
                <Logo />
            </div>
        </div>
        <h1>
            Turbodev.app
        </h1>
        <p>
            web, e-commerce, mobile
        </p>
    </div>
</div>


<style>
    h1,
    p {
        text-align: center;
        text-shadow: 2px 2px 2px rgba(0, 0, 0, 0.05),
               -2px -2px 2px rgba(0, 0, 0, 0.05),
               2px -2px 2px rgba(0, 0, 0, 0.05),
               -2px 2px 2px rgba(0, 0, 0, 0.05);
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
        width: 100vw;
        height: 100vh;
        display: flex;
        align-items: center;
        justify-content: center;
        padding: .5rem;
    }
    /*
    .engine {
        width: 300px;
        height: 300px;
        border-radius: 50%;
        overflow: hidden;
        position: relative;
    }
    .logo{
        position: absolute;
        top: 0px;
        left: -25px;
        z-index: 1;
    } */
</style>