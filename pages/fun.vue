<template>
  <div>
    <div class="bg-red-200">
      je suis là que pour les tests
      <ContactPlugin />
    </div>
  </div>
</template>

<script>
import ContactPlugin from '@/components/ContactPlugin.vue'
export default {
  name: 'FunPage',
  components: {
    ContactPlugin
  },
  title: 'fun for fun'
}
</script>
