<script>
 let user = {loggedIn:false};

  function toggle(){
    user.loggedIn = !user.loggedIn;
  }
</script>
<h1>Log in using 'else', a continuation</h1>
<!-- if logged in you can log out-->
{#if user.loggedIn}
<button on:click={toggle}>
  Log-Out *.*
</button>
{:else} <!--'{:else} is a a continuation of a tag'-->
<button on:click={toggle}>
  Log-In
</button>
{/if}
<hr>

<!--look at the code below see a code without '{:else}'-->
<h1>Log in and Log out without 'else'</h1>
<!-- if logged in you can log out-->
{#if user.loggedIn}
<button on:click={toggle}>
  Log Out
</button>
{/if}

<!-- if are not logged in you can log in-->
{#if !user.loggedIn}
<button on:click={toggle}>
  Log In
</button>
{/if}