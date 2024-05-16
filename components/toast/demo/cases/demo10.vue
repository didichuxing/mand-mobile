<template>
  <div class="md-example-child md-example-child-toast md-example-child-toast-10">
    <md-button @click="showWarningToast">警告</md-button>
  </div>
</template>

<script>import {Toast, Button} from 'mand-mobile'

export default {
  name: 'toast-demo',
  /* DELETE */
  title: '警告',
  titleEnUS: 'Success',
  /* DELETE */
  components: {
    [Button.name]: Button,
  },
  methods: {
    showWarningToast() {
      Toast.warning('操作警告')
    },
  },
}
</script>
