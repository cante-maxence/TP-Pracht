<template>
  <nav>
    <h4 class="text-xl">
      <Bars3Icon class="inline-block h-5 w-5 text-blue-500" />
      
      menu (dans <code class="font-mono">/src/App.vue</code>)
    </h4>
    <ul>
      <li>
        <br>
<hr>
         
            <hr>
        <Router-link to="/listeJson"/>
        <hr>
        <Router-link to="/new"/>
        <hr>
        
        <hr>
        <br>
      </li>
    </ul>
  </nav>

<a href="simple">Page simple</a>
<br><br>
<a href="new">Page new</a>
<br><br>
<a href="liste">Page liste</a>

<br><br>
<a href="listeJson">Page listeJson</a>
<br><br>
<a href="liste-supabase">Page liste-supabase</a>
<br><br>
<a href="id">Page id</a>






  <!-- Affiche les pages -->
   <Suspense>
  <RouterView class="m-2 border-2 p-2" />
   </Suspense>
</template>

<script setup lang="ts">
</script>
