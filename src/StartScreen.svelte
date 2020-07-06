<script>
    const posters = [
        {
            title: 'AIWS',
            logo: 'static/gif/AIWS transp from Encoder.gif',
            banner: 'static/banners/AIWS banner wide.png',
            bannerBlur: 'static/banners/AIWS banner wide blur.png',
        },
        {
            title: 'SYN',
            logo: 'static/gif/SYN transp from Encoder.gif',
            banner: 'static/banners/SYN banner wide.png',
            bannerBlur: 'static/banners/SYN banner wide blur.png',
        },
        {
            title: 'RTI',
            logo: 'static/gif/RTI Transp from Encoder.gif',
            banner: 'static/banners/RTI banner wide.png',
            bannerBlur: 'static/banners/RTI banner wide blur.png',
        },
    ];
</script>

<style>
    .wrapper {
        display: flex;
        height: calc(100vh - 100px);
    }

    .poster {
        position: relative;
        display: flex;
        justify-content: center;
        width: calc(1/3 * 100%);
    }

    .poster_logo {
        position: absolute;
        top: 180px;
        width: 100%;
    }

    .poster_banner,
    .poster_bannerBlur {
        position: absolute;
        width: 100%;
    }

    .poster_bannerBlur:hover {
        opacity: 0;
    }
</style>

<div class="wrapper">
    {#each posters as poster}
        <div class="poster">
            <img class="poster_banner" src={poster.banner} alt='' />
            <img class="poster_bannerBlur" src={poster.bannerBlur} alt='' />
            <img class="poster_logo" src={poster.logo} alt='' />
        </div>
    {/each}
</div>