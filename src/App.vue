<template>
  <div id="app" >
    <div class="container">
      <div class="row  main-content">
        <div v-for="(productItem, index) in productItems" :key="index" class="col-xl-3 col-lg-4 col-md-6 col-sm-12 col-12">
          <productItem :product="productItem"></productItem>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import './assets/style/font.css'
// import './assets/style/style1.css'
// import './assets/style/style2.css'
import productItem from './components/productItem.vue'
export default {
  data(){
    return {
      productItems:[
        {
          image: 'https://cdn.alaatv.com/upload/images/product/01_20210510085445.jpg?w=331&h=331',
          title: 'همایش آرش جمع بندی ',
          author: 'محمد صادق ثابتی',
          duration: '۲۰ ساعت',
          price: {
            base: 12000000,
            final: 11500000,
          },
        },
        {
          image: 'https://cdn.alaatv.com/upload/images/product/02_20210510085432.jpg?w=331&h=331',
          title: 'همایش آرش جمع بندی علوم و فنون ادبی کنکور',
          author: 'محمد صادق ثابتی',
          duration: '۲۰ ساعت',
          price: {
            base: 12000000,
            final: 11500000,
          },
        },
        {
          image: 'https://cdn.alaatv.com/upload/images/product/07_20210510085547.jpg?w=331&h=331',
          title: 'همایش آرش جمع بندی علوم و فنون ادبی کنکور',
          author: 'محمد صادق ثابتی',
          duration: '۲۰ ساعت',
          price: {
            base: 12000000,
            final: 11500000,
          },
        },
        {
          image: 'https://cdn.alaatv.com/upload/images/product/08_20210510085456.jpg?w=331&h=331',
          title: 'همایش آرش جمع بندی علوم و فنون ادبی کنکور',
          author: 'محمد صادق ثابتی',
          duration: '۲۰ ساعت',
          price: {
            base: 12000000,
            final: 11500000,
          },
        },
        {
          image: 'https://cdn.alaatv.com/upload/images/product/12_20210510085405.jpg?w=331&h=331',
          title: 'همایش آرش جمع بندی علوم و فنون ادبی کنکور',
          author: 'محمد صادق ثابتی',
          duration: '۲۰ ساعت',
          price: {
            base: 12000000,
            final: 11500000,
          },
        },
        {
          image: 'https://cdn.alaatv.com/upload/images/product/11_20210510085516.jpg?w=331&h=331',
          title: 'همایش آرش جمع بندی علوم و فنون ادبی کنکور',
          author: 'محمد صادق ثابتی',
          duration: '۲۰ ساعت',
          price: {
            base: 12000000,
            final: 11500000,
          },
        },
        {
          image: 'https://cdn.alaatv.com/upload/images/product/06_20210510085352.jpg?w=331&h=331',
          title: 'همایش آرش جمع بندی علوم و فنون ادبی کنکور',
          author: 'محمد صادق ثابتی',
          duration: '۲۰ ساعت',
          price: {
            base: 12000000,
            final: 11500000,
          },
        },
        {
          image: 'https://cdn.alaatv.com/upload/images/product/02_20210510085432.jpg',
          title: ' همایش آرش جمع بندی علوم و فنون ادبی کنکورهمایش آرش جمع بندی علوم و فنون ادبی کنکورهمایش آرش جمع بندی علوم و فنون ادبی کنکورهمایش آرش جمع بندی علوم و فنون ادبی کنکور',
          author: 'محمد صادق ثابتی',
          duration: '۲۰ ساعت',
          price: {
            base: 12000000,
            final: 11500000,
          },
        }
      ]
    }
  },
  name: 'App',
  components: {
    productItem
  }
}
</script>
<style scoped>
.main-content{
  margin-top: 100px;
}
#app{
  width: 100%;
  height: 100%;
}

</style>
