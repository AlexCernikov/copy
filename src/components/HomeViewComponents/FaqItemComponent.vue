<template>
    <div class="faq-item">
        <h6 class="faq-item__title">{{name}}</h6>
        <button class="faq-item__btn">
            <img src="../../assets/faqsection/arrow-down.svg" alt="arrow">

        </button>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'FaqComponent',
  props: {
    name: {
      type: String,
    },
  },
});
</script>
<style scoped lang="scss">
@import "../../../public/scss/styles.scss";
.container{
    max-width: 1100px;
    margin: auto;
}
a{
  text-decoration: none;
}
.faq-item{
    border: 1px solid black;
    width: 350px;
    height: 170px;
    &__title{
        font-family: 'Roboto Condensed';
        font-style: normal;
        font-weight: 400;
        font-size: 26px;
        line-height: 30px;
        text-align: center;
        
    }
    &__btn{
        border: none;
        background-color: $btn-color;
    }
}
</style>
