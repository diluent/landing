<script>
    import MenuButton from "./MenuButton.svelte";

    export let onCloseClick;
    export let onMenuElementClick;
</script>

<style>
    .menu {
        position: fixed;
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, .8);
        z-index: 1;
    }

    .menu_list {
        position: fixed;
        top: 200px;
        left: 50%;
        color: #fff;
    }

    .menu_list-item {
        font-family: 'TGPraktikal', Arial, sans-serif;
        font-weight: normal;
        font-style: normal;
        font-size: 24pt;
        padding-bottom: 15px;
        cursor: pointer;
    }

    .menu_button {
        position: absolute;
        right: 20px;
        top: 20px;
    }
</style>

<div class="menu" on:click={onCloseClick}>
    
    <div class="menu_button">
        <MenuButton onClick={onCloseClick} color={'white'}/>
    </div>

    <div class="menu_list">
        <div class="menu_list-item" on:click={() => onMenuElementClick('home')}>HOME</div>
        <div class="menu_list-item" on:click={() => onMenuElementClick('synthesia')}>SYNETHESIA</div>
        <div class="menu_list-item" on:click={() => onMenuElementClick('theRoomTiltIllusion')}>THE ROOM TILT ILLUSION</div>
        <div class="menu_list-item" on:click={() => onMenuElementClick('aliceInWonderland')}>ALICE IN WONDERLAND</div>
    </div>
</div>