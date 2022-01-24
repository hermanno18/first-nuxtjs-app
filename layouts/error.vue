<template>
  <div>
    <h1 v-if="error.statusCode === 404">
      Page non trouvée
    </h1>
    <h1 v-else>
      Une erreur est survenue
    </h1>
    <NuxtLink to="/">
      Page d'accueil
    </NuxtLink>
  </div>
</template>

<script>
export default {
  layout: 'error', // nous pouvons definir un layout personnalisé pour la page erreur
  props: ['error']
}
</script>
