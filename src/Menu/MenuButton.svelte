<script>
    export let onClick;
    export let color;

    const onMenuButtonClick = () => {
        console.log('111')
        showMenu = !showMenu;
    };
</script>

<style>
    .menuButton {
        cursor: pointer;
        z-index: 2;
        /* position: absolute;
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, .4);
        z-index: 1; */
    }
</style>

<div class="menuButton" on:click={onClick}>
    <svg width="90" height="30" viewBox="0 0 379 176" fill="none" xmlns="http://www.w3.org/2000/svg">
        <rect width="379" height="44" fill={color}/>
        <rect y="132" width="379" height="44" fill={color}/>
        <rect y="66" width="379" height="44" fill={color}/>
    </svg>
</div>