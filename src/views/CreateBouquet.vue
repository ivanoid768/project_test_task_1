<template>
  <div class="create-bouquet">
    <div class="header">
      <h1>Новый букет</h1>
      <div class="close-btn">&#x274C;</div>
    </div>

    <form>
      <div class="form-group">
        <ImageInput></ImageInput>
      </div>

      <div class="form-group">
        <label for="avaliable">Наличие</label>
        <Select></Select>
      </div>

      <div class="form-group">
        <label for="name">Название</label>
        <input type="text" id="name" placeholder="Маленький розовый">
      </div>

      <div class="form-group">
        <label for="description">Описание</label>
        <TextArea></TextArea>
      </div>

      <div class="form-group">
        <label for="price">Цена, Т</label>
        <input type="number" id="price" placeholder="10200">
      </div>

      <div class="form-group">
        <label for="composition">Состав</label>
        <!-- <input type="number" id="composition"> -->
        <MultiSelect></MultiSelect>
      </div>

      <div class="form-group">
        <label for="color">Состав</label>
        <!-- <input type="number" id="color"> -->
        <Select></Select>
      </div>

      <button type="submit" class="btn btn-primary">Опубликовать</button>
    </form>
  </div>
</template>

<script>
  // @ is an alias to /src
  import Select from '@/components/Select.vue';
  import MultiSelect from '@/components/MultiSelect.vue';
  import ImageInput from '@/components/ImageInput.vue';
  import TextArea from '@/components/TextArea.vue';

  export default {
    name: 'create_bouquet',
    components: {
      Select,
      MultiSelect,
      ImageInput,
      TextArea
    },
  };
</script>

<style lang="scss" scoped>
  .header {
    display: flex;
    justify-content: space-between;
    margin-bottom: 40px;

    h1 {
      font-size: 28px;
      font-family: "Open Sans", sans-serif;
      font-style: normal;
      font-weight: normal;
      margin: 0px;
    }
    .close-btn {
      font-size: 28px;
      cursor: pointer;
      font-family: "Open Sans", sans-serif;
      font-style: normal;
      font-weight: normal;
    }
  }
  .create-bouquet {
    width: 320px;
    margin: auto;
    text-align: initial;
    padding: 16px 15px;
    border: 1px solid #eee;
  }
</style>
