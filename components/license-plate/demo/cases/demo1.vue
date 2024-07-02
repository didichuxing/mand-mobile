<template>
  <div>
    <!-- 投保人车牌号 -->
    <md-field title="车辆信息">
      <div @click="changeNumber">
        <md-detail-item title="车牌号码">
          {{ licensePlate }}
        </md-detail-item>
      </div>
    </md-field>
    <md-license-plate
      :modeShow="'popUp'"
      :showPopUp="showPopUp"
      @hide="hide"
      @confirm="confirm"
      @onEnter="onEnter"
      @onDelete="onDelete"
    >
    <template v-slot:content>
      <md-button
        class="go-to-quote"
        :disabled="buttonDisabled"
        :class="[buttonDisabled ? 'buttonDisabled' : '']"
        type="primary"
      >
        查看报价
      </md-button>
    </template>
    </md-license-plate>
  </div>
</template>

<script>
import {LicensePlate, DetailItem, Field, Button} from 'mand-mobile'

export default {
  name: 'license-plate-demo',
  title: '半弹层版',
  components: {
    [LicensePlate.name]: LicensePlate,
    [DetailItem.name]: DetailItem,
    [Field.name]: Field,
    [Button.name]: Button,
  },
  data() {
    return {
      showPopUp: false,
      licensePlate: '',
      buttonDisabled: false,
    }
  },
  methods: {
    hide() {
      this.showPopUp = false
    },
    changeNumber() {
      this.showPopUp = true
    },
    confirm(value) {
      this.hide()
      this.licensePlate = value
    },
    onEnter(value) {
      this.licensePlate = value
    },
    onDelete(value) {
      this.licensePlate = value
    },
  },
}

</script>


<style lang="stylus" scoped>
.md-button {
  width: 670px;
  height: 100px;
  border-radius: 50px;
  background: #198CFF;
  border 0
  margin 0 auto
  margin-bottom 40px
}
.md-button.block {
  width: 670px;
}
.md-button.primary:after {
  border 0
}
>>>.md-license-plate-input .md-license-plate-input-item {
  width 72px
}
.buttonDisabled
  >>>.primary
    box-shadow none
    opacity: 1;
    background: rgba(25, 140, 255, 0.3);
</style>
