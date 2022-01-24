<template>
  <div class="absolute right-0 bottom-0 ">
    <div class="relative">
      <div v-for="button in buttons" :key="button" class="flex justify-end">
        <BtnContactPlugin v-if="button.for != 'close' && button.for != 'message' && displayAll" :button="button" />
      </div>
    </div>
    <div class="horizontal flex ">
      <div v-for="button in buttons" :key="button">
        <BtnContactPlugin v-if="button.for === 'message' && displayAll" :button="button" />
        <BtnContactPlugin v-if="button.for === 'close'" :button="button" :toggle="toggle" />
      </div>
    </div>
  </div>
</template>

<script>
import BtnContactPlugin from './BtnContactPlugin.vue'

export default {
  components: {
    BtnContactPlugin
  },
  data () {
    return {
      buttons: [
        {
          for: 'phone',
          bgColor: 'bg-green-500',
          textColor: 'text-white',
          icon: 'fas fa-phone'
        },
        {
          for: 'mail',
          bgColor: 'bg-red-500',
          textColor: 'text-white',
          icon: 'far fa-envelope'
        },
        {
          for: 'messenger',
          bgColor: 'bg-blue-600',
          textColor: 'text-white',
          icon: 'fab fa-facebook-messenger'
        },
        {
          for: 'user',
          bgColor: 'bg-green-800',
          textColor: 'text-white',
          icon: 'fas fa-user'
        },
        {
          for: 'message',
          bgColor: 'bg-green-800',
          textColor: 'text-white',
          icon: 'fas fa-comment-alt'
        },
        {
          for: 'close',
          bgColor: 'bg-green-800',
          textColor: 'text-white',
          icon: 'fas fa-times'
        }
      ],
      displayAll: false
    }
  },
  methods: {
    toggle () {
      this.displayAll = !this.displayAll
    }
  }
}
</script>
