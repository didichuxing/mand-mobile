<template>
  <div class="md-example-child md-example-child-amount">
    <md-amount
      :value="1234"
      mask
      precision="0"
    ></md-amount>
    <br>
	</div>
</template>

<script>import {Amount} from 'mand-mobile'

export default {
  name: 'amount-demo',
  /* DELETE */
  title: '掩码展示',
  titleEnUS: 'Mask Display',
  /* DELETE */
  components: {
    [Amount.name]: Amount,
  },
}
</script>

<style lang="stylus" scoped>
.md-example-child-amount
  text-align center
  font-size 32px
  color #666
</style>
