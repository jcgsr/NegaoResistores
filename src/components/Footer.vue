<template>
   <footer class="footer alert alert-secondary">
      <p>&copy;2020 - {{ msg }}</p><a :href="link" class="btn btn-primary">Jovane</a>
   </footer>
</template>

<script>
export default {
   data() {
      return {
         msg: 'WebApp do Negão para calcular Resistores criado por ',
         link: 'https://jcgsr.github.io/'
      }
   }
}
</script>

<style>
.footer {
   width: 100%;   
   margin-top: 4rem;   
   text-align: center;
}

.footer p {
   color: rgb(25, 25, 53);
}

.footer a {
   width: 6rem;
   font-size: smaller;
}

.footer a:link{
   text-decoration: none;
}
</style>