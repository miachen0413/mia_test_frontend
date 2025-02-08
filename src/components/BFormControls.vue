<template>
  <div>
    <label for="" class="form-label"></label>
    <input type="" :value="modelValue" @input="setInputValue"  class="form-control" id="" placeholder="">
  </div>
</template>

<script>
export default {
  props:["modelValue"],
  emits: ["update:modelValue"],
  data() {
    return {
      value: ''
    }
  },
  methods:{
    setInputValue(e){
      this.$emit("update:modelValue", e.target.value)
    }
  }

}
</script>

<style lang="scss" scoped></style>