<script>
  import { onMount } from "svelte";
  import StartScreen from "./StartScreen.svelte";
  import SecondScreen from "./components/SecondScreen.svelte";
  // import ThirdScreen from "./ThirdScreen.svelte";
  import Header from "./Header.svelte";

  // run this when the app starts
  onMount(() => {});

  let currentPage = null;

  const onMenuElementClick = page => currentPage = page;
</script>

<style>
  @font-face {
    font-family: "TGPraktikal";
    src: url("static/fonts/TGPraktikal-Medium.otf");
  }

  header {
    height: 100px;
  }
</style>

<header>
  <Header onMenuElementClick={onMenuElementClick} />
</header>

<main>

  <!-- <UserSearch /> -->

  <!-- {#if users}
  <ul class="user-list">
    {#each users as user}
      <li>
        <User username={user.login} avatar={user.avatar_url} />
      </li>
    {/each}
  </ul>
  {/if} -->

  {#if currentPage == null || currentPage === 'home'}
    <StartScreen />
  {:else}
    <SecondScreen poster={currentPage}/>
  {/if}
  <!-- <ThirdScreen /> -->
  
</main>