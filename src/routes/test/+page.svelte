<script>
    let targetElement;

    function scrollToElement() {
        if (targetElement) {
            targetElement.scrollIntoView({ behavior: "smooth" });
        }
    }
</script>

<style>
    .spacer {
        height: 200vh; /* This is to create some space to scroll */
    }
</style>

<div class="spacer"></div>
<button on:click={scrollToElement}>Scroll to Element</button>
<div bind:this={targetElement} style="margin-top: 100vh;">
    This is the target element.
</div>
<div class="spacer"></div>
