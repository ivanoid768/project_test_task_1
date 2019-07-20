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
        <Select :options="availableOpts" v-model="available"></Select>
      </div>

      <div class="form-group">
        <label for="name">Название</label>
        <input v-model="name" type="text" id="name" placeholder="Маленький розовый">
      </div>

      <div class="form-group">
        <label for="description">Описание</label>
        <TextArea></TextArea>
      </div>

      <div class="form-group">
        <label for="price">Цена, Т</label>
        <input v-model="price" type="number" id="price" placeholder="10200">
      </div>

      <div class="form-group">
        <label for="composition">Состав</label>
        <!-- <input type="number" id="composition"> -->
        <MultiSelect></MultiSelect>
      </div>

      <div class="form-group">
        <label for="color">Цвет</label>
        <!-- <input type="number" id="color"> -->
        <Select :options="colorOpts" v-model="color"></Select>
      </div>

      <button type="submit" class="btn btn-primary">Опубликовать</button>
    </form>
  </div>
</template>

<script>
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
    data() {
      return {
        organizationId: 8,
        name: "",
        price: null,
        description: "",
        height: 10,
        mainImage: null,
        subtitle: "",
        url: "",  //"/my_beauriful_bouquet"
        cityCodes: "", // ["astana"]
        categoriesIds: "", // [1, 2]
        available: '0',
        color: '0',
        availableOpts: [],
        compositionOpts: [],
        colorOpts: []
      }
    },
    created() {
      this.availableOpts = [
        { name: 'Есть в наличии' },
        { name: 'Нет в наличии' }
      ];

      this.colorOpts = [
        { name: 'Красный' },
        { name: 'Розовый' }
      ];

    }
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
