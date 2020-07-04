<script>
    import MenuButton from "./MenuButton.svelte";

    export let onCloseClick;
</script>

<style>
    .menu {
        position: absolute;
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, .4);
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
    }

    .menu_button {
        position: absolute;
        right: 20px;
        top: 20px;
    }
</style>

<div class="menu">
    
    <div class="menu_button">
        <MenuButton onClick={onCloseClick} color={'white'}/>
    </div>

    <div class="menu_list">
        <div class="menu_list-item">HOME</div>
        <div class="menu_list-item">SYNETHESIA</div>
        <div class="menu_list-item">THE ROOM TILT ILLUSION</div>
        <div class="menu_list-item">ALICE IN WONDERLAND</div>
    </div>
</div>