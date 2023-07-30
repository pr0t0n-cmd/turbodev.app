<script>
  import Bubble from "./Bubble.svelte";
    // export let buttonClassNames
    // export let textClassNames
</script>
<button id="gooey-button" class="relative py-6 px-2 text-2xl bg-[#f00] text-black border-none outline-none">
    <span>Ciao</span>
    <span class="bubbles absolute top-0 left-0 bottom-0 right-0">
        <Bubble />
        <Bubble />
        <Bubble />
    </span>
    <svg xmlns="http://www.w3.org/2000/svg" version="1.1" class="h-0">
        <defs>
            <filter id="gooey">
                <feGaussianBlur in="SourceGraphic" stdDeviation="5" result="blur" />
                <feColorMatrix in="blur" type="matrix" values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 19 -9" result="highContrastGraphic" />
                <feComposite in="SourceGraphic" in2="highContrastGraphic" operator="atop" />
            </filter>
        </defs>
    </svg>
</button>

<style> 
  #gooey-button {
    filter: url('#gooey');
  }
</style>