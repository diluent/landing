<script>
    const posters = [
        {
            title: 'synesthesia',
            src: 'img/img1.jpg',
        },
        {
            title: 'RTI',
            src: 'img/img2.jpg',
        },
        {
            title: 'AIWS',
            src: 'img/img3.jpg',
        }
    ];
</script>

<style>
    .wrapper {
        display: flex;
    }

    .poster {
        display: flex;
        justify-content: center;
        width: 33%;
    }

    .poster img {
        width: 90%;
    }
</style>

<div class="wrapper">
    {#each posters as poster}
        <div class="poster">
            <!-- <p>{poster.title}</p> -->
            <img src={poster.src} alt={poster.title} />
        </div>
    {/each}
</div>