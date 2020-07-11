<script>
    export let poster;

    const posters = {
        aliceInWonderland: {
            title: 'AIWS',
            logo: 'static/gif/AIWS transp from Encoder.gif',
            banner: 'static/banners/AIWS banner wide.png',
        },
        synthesia: {
            title: 'SYN',
            logo: 'static/gif/SYN transp from Encoder.gif',
            banner: 'static/banners/SYN banner wide.png',
        },
        theRoomTiltIllusion: {
            title: 'RTI',
            logo: 'static/gif/RTI Transp from Encoder.gif',
            banner: 'static/banners/RTI banner wide.png',
        },
    };
</script>

<style>
    .wrapper {
        height: calc(100vh - 100px);
        position: relative;
    }

    .poster_logo_wrapper {
        position: absolute;
        top: 100px;
        width: 100%;
        height: calc(100vh - 300px);
        background-color: #000;
        display: flex;
        justify-content: center;
    }

    .poster_logo {
        height: calc(100vh - 300px);
    }

    .poster_background {
        display: flex;
        height: calc(100vh - 100px);
    }

    .poster_left {
        width: 50vw;
    }

    .poster_right {
        transform: scaleX(-1);
        width: 50vw;
    }
</style>

<div class="wrapper">
    <div class="poster_background">
        <img class="poster_left" src={posters[poster].banner} alt='' />
        <img class="poster_right" src={posters[poster].banner} alt='' />
    </div>
    <div class="poster_logo_wrapper">
        <img class="poster_logo" src={posters[poster].logo} alt='' />
    </div>
</div>
