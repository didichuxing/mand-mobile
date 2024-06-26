<template>
  <div class="md-example-child md-example-child-toast md-example-child-toast-0">
    <md-button @click="showTextToast">纯文字</md-button>
  </div>
</template>

<script>
import {Toast, Button} from 'mand-mobile'

export default {
  name: 'toast-demo',
  /* DELETE */
  title: '纯文字',
  titleEnUS: 'Plain text',
  /* DELETE */
  components: {
    [Button.name]: Button,
  },
  methods: {
    showTextToast() {
      Toast.info('申请成功，结清证明将于3个工作日后发送到您的接收邮箱刘龙')
    },
  },
}

</script>
