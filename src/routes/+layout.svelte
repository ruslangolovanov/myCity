<nav>
    <div class="nav-container">
      <a href="/" class="nav-logo" title="Back to Homepage">Казань</a>
         <div class="nav-links">
             {#each nav as link}
               {#if link.isShow}
                  <a href = {link.href} class="link">{link.title}</a>
               {/if}
             {/each}
         </div>
    </div>
</nav>

<script>
    import { each,  } from "svelte/internal";
  
      const nav = [
          {
              title : "Фотографии",
              href : "/about",
              isShow : true
          },
          {
              title : "История",
              href : "/blog",
              isShow : true
          },
          {
              title : "Достопримечательности",
              href : "/project",
              isShow : true
          },
          {
              title : "Учебные заведения",
              href : "/contact",
              isShow : true
          }
      ]
  </script>
  

<div class="container">
    <!-- Pages will be injected below --> 
    <slot></slot>
</div>

<style>
    .container {
    max-width: 1400px; margin: 50px auto;
    }

    nav{
        background-color: #ecebe8;
        width: 100%;
        max-width: 1400px;
        margin: 0 auto;
        position: sticky;
        border-radius: 10px;
    }

    .nav-logo{
        margin: 0 60px;
    }
</style>