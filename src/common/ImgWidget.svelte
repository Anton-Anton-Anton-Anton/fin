<script>

    export let text;
    export let imgSrc;
    export let widthC;


</script>

<div>
    <img src={imgSrc} alt={text}>
</div>

<style>

img {
    border: 1px solid darkgray;
    min-width: 100%;
    max-width: 100%;
    height: auto;
    border-radius: 8px;
}

</style>