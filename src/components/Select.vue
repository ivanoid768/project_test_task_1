<template>
  <select name="sel_1" id="sel_1">
    <option value="1">Есть в наличии</option>
    <option value="2">option_2</option>
    <option value="3">option_3</option>
  </select>
</template>

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
