<template>
    <div class="faq-item" @click="goToPage" @keypress="bar">
        <h6 class="faq-item__title">{{name}}</h6>
        <button class="faq-item__btn">
            <!-- <img class="faq-item__btn-arrow arrow"
            src="../../assets/faqsection/arrow-down.svg" alt="arrow"> -->
            <div class="faq-item__btn-arrow"></div>
        </button>
        <div class="faq-item__hover"></div>
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
  methods: {
    goToPage() {
      this.$router.push('/ourSpaces');
    },
  },
});
</script>
<style scoped lang="scss">
@import "../../../public/scss/styles.scss";
*{
  box-sizing: border-box;
}
.container{
    max-width: 1100px;
    margin: auto;
}
a{
  text-decoration: none;
}
.faq-item{
    width: 350px;
    height: 170px;
    position: relative;
    margin-bottom: 65px;
    cursor: pointer;
    padding: 40px 40px;
    &__title{
      font-family: 'Roboto Condensed';
      font-style: normal;
      font-weight: 400;
      font-size: 26px;
      line-height: 30px;
      text-align: center;
      margin: 0;
    }
    &__btn{
      position: absolute;
      bottom: -24px;
      left: 50%;
      transform:translate(-50%);
      border: none;
      background-color: $btn-color;
      width: 64px;
      height: 47px;
      display: flex;
      align-items: center;
      justify-content: center;
      align-self: center;
      cursor: pointer;
    }
    &__btn-arrow{
      mask: url(../../assets/faqsection/arrow-down.svg);
      background: #ffffff;
      width: 16px;
      height: 10px;
      mask-size: cover;
    }
    &__hover{
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background-color:$btn-color;
      color:#ffffff;
      padding: 40px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      opacity: 0;
      z-index: -1;
      transition: all .6s;
    }
    &:hover{
      color: #ffffff;
    }
    &:hover  .faq-item__hover{
      opacity: 1;
    }
    &:hover  .faq-item__btn{
      background: #ffffff;
      box-shadow: -8px 2px 18px 7px rgb(255 90 0 / 21%);
    }
    &:hover  .faq-item__btn-arrow{
      background-color: $btn-color;
    }
}
</style>
