<script>
  import { onMount } from "svelte";
  import StartScreen from "./StartScreen.svelte";
  import Header from "./Header.svelte";
  // import UserSearch from "./UserSearch.svelte";

  // create a variable to store our users
  let users;

  // run this when the app starts
  onMount(() => {
    getGitHubUsers();
  });

  /**
   * Grab users from GitHub
   */
  function getGitHubUsers() {
    fetch("https://api.github.com/users")
      .then(resp => resp.json())
      .then(data => (users = data));
  }
</script>

<style>
  @font-face {
    font-family: "TGPraktikal";
    src: url("static/fonts/TGPraktikal-Medium.otf");
  }
</style>

<header>
  <Header />
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

  <StartScreen />
  
</main>