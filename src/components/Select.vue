<template>
  <select @change="onChange" name="sel_1" id="sel_1" :value="value">
    <option v-for="(option, index) in options" :key="index" :value="index">
      <span> {{option.name}} </span>
    </option>
  </select>
</template>

<script>
  export default {
    props: {
      options: Array,
      value: String,
    },
    methods: {
      onChange(e) {
        this.$emit('input', e.target.value)
      }
    }
  }
</script>


<style lang="scss" scoped>
  select {
    border: none;
    border-bottom: 1px solid #e1e1e1;
    flex-basis: 100%;

    font-family: "Open Sans", sans-serif;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 22px;
    color: #000000;

    option {
      font-family: "Open Sans", sans-serif;
      font-style: normal;
      font-weight: normal;
      font-size: 16px;
      line-height: 22px;
      color: #000000;
    }

    &:focus {
      outline: none;
    }
  }
</style>
