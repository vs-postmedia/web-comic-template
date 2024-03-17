<script>
    export let image;
    export let align;
    export let id;
    export let imageAlt
    export let maxWidth;
    export let source;
    export let quoteText;

    const string = `<span class="opening-quote">“</span>${quoteText}”`;
</script>


<div class="panel full no-border" id={id}>
    <div class="quote-block-container">
        <div class="image-quote-block center {align}">
            <img src={image} class={align} style="max-width:{maxWidth}" alt={imageAlt}/>
            <p class="quote-text center">{@html string}</p>
        </div>
        {#if source}
            <p class="name-title">– {source}</p>
        {/if}
    </div>
</div>

<style>
    .quote-block-container {
        margin: 0 auto;
    }
    .image-quote-block {
        border: 4px solid var(--brite_purple01);
        position: relative;
    }
    #container .image-quote-block .quote-text {
        position: relative;
    }
    :global(.opening-quote) {
        color: var(--brite_purple01);
        font-size: 2rem;
    }
    :global(#app .panel .name-title) {
        color: var(--grey01);
        font-family: 'BentonSansCond-RegItalic', italic;
        margin: 5px 0 0 auto;
        max-width: 75%;
        /* position: absolute; */
        right: 5px;
        text-align: right;
    }
    :global(#app .image-quote-block p) {
        color: #6D6E70;
        font-family: 'Shift-BoldItalic';
        font-size: 1.2rem;
        padding: 3px 2px;
    }

    .image-quote-block img {
        border: 3px solid rgba(255,255,255,0.7);
        border-radius: 50%;
        filter: grayscale(1) drop-shadow(4px 6px 6px rgba(155,63,134,0.4)) brightness(1);
        height: 35%;
        max-width: 175px;
        width: 35%;
    }
    .image-quote-block img.right {
        float: right;
        margin: -15px -10px 10px 10px;
    }
    .image-quote-block img.left {
        float: left;
        margin: -15px 10px 10px -20px;
    }

    /* MEDIA QUERIES */
@media only screen and (min-width: 550px) {
    .quote-block-container {
        width: 80%
    }
    :global(#app .panel .name-title) {
        margin-top: 10px;
        width: 80%;
    }
    .panel .name-title {
        margin: 7px 10% 0 40%;
    }
    .image-quote-block.left img {
        left: -25px;
    }
}
</style>