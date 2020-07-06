<script>
    import Menu from "./Menu/Menu.svelte";
    import MenuButton from "./Menu/MenuButton.svelte";

    let showMenu = false;

    const onMenuButtonClick = () => showMenu = !showMenu;

</script>

<style>
    .header {
        position: fixed;
        display: flex;
        justify-content: center;
        top: 0;
        left: 0;
        height: 100px;
        width: 100%;
        background-color: #fff;
        z-index: 1;
    }

    .header_logo {
        position: absolute;
        height: 220px;
        top: -70px;
    }

    .menu_button {
        position: absolute;
        right: 20px;
        top: 20px;
    }
</style>

<div class="header">
    <img class="header_logo" src="static/logo/black_tittel1.png" alt="" />
    <img class="header_logo" src="static/logo/black_tittel2 destort.png" alt="" />

    {#if (showMenu)}
        <Menu onCloseClick={onMenuButtonClick} />
    {:else}
        <div class="menu_button">
            <MenuButton onClick={onMenuButtonClick} color={'black'}/>
        </div>
    {/if}
</div>