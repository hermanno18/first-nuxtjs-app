<template>
  <div v-if="button.for==='close'" class="">
    <div :class="'p-2 rounded-full h-9 w-9 flex place-content-center items-center m-1 ' + button.bgColor + ' ' + button.textColor" @click="toggle">
      <i :class="' '+button.icon" />
    </div>
  </div>
  <div v-else class="">
    <div :class="'p-2 rounded-full h-9 w-9 flex place-content-center items-center m-1 ' + button.bgColor + ' ' + button.textColor">
      <i :class="' '+button.icon" />
    </div>
  </div>
</template>

<script>

export default {
  name: 'BtnContactPlugin',
  props: ['button', 'toggle']
}

</script>
