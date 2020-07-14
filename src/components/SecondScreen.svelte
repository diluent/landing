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

    .row {
        padding: 40px 20px;
        display: flex;
    }

    .second_screen_banner_wrapper {
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

    .video1 {
        width: 100%;
    }
</style>

<div>
    <div class="second_screen_banner_wrapper">
        <div class="poster_background">
            <img class="poster_left" src={posters[poster].banner} alt='' />
            <img class="poster_right" src={posters[poster].banner} alt='' />
        </div>
        <div class="poster_logo_wrapper">
            <img class="poster_logo" src={posters[poster].logo} alt='' />
        </div>
    </div>

    <div class="row">
        <div style="width: 60%; margin-right: 20px;">
            <video
                style="width: 100%;"
                src="static/videos/1.mp4"
                type="video/mp4"
                muted
                autoplay
                loop
            />
        </div>
        <div>What is synesthesia?</div>
    </div>

    <div class="row">
        <div style="width: 25%; overflow: hidden; position: relative; margin-right: 40px; margin-left: 250px;">
            <video
                style="width: 1200px; position: absolute; left: -430px;" 
                src="static/videos/2.mp4"
                type="video/mp4"
                muted
                autoplay
                loop
            />
        </div>
        <div style="width: 75%;">
            <div style="padding: 20px 40px 20px 20px; text-align: right;">The causes of the phenomenon</div>
            <div>
                <img src="static/screen2/2.png" alt="" />
            </div>
        </div>

    </div>
</div>
