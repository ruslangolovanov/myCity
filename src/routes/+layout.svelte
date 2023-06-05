<nav>
    <div class="nav-container">
      <a href="/" class="nav-logo" title="Back to Homepage">Казань</a>
         <div class="nav-links">
             {#each nav as link}
               
                  <a href = {link.href} class="link">{link.title}</a>
               
             {/each}
         </div>
    </div>
</nav>

<script>
    import { each,  } from "svelte/internal";
  
      const nav = [
          {
              title : "Фотографии",
              href : "/photos",
              
          },
          {
              title : "История",
              href : "/history",
             
          },
          {
              title : "Достопримечательности",
              href : "/atractions",
          },
          {
              title : "Учебные заведения",
              href : "/vuz",
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