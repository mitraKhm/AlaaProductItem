<template>
  <div class="product-item-box ">
    <div class="product-item-main-box">
      <a href="#" class="img-box">
        <img :src="product.image" class="img" alt="img1">
      </a>
      <div class="product-item-content">
        <div class="main-title">
          <a href="#" class="title-box">
        <span class="title-text">
           {{product.title }}
        </span>
          </a>
        </div>
        <div class="time-author-box">
          <div  class="box-item">
            <img src="../assets/icons/teacher.png" class="teacher-icon" alt="img1">
            <span class="author">
          {{ product.author }}
         </span>
          </div>
          <div class="box-item">
            <img src="../assets/icons/time.png" class="time-icon" alt="img1">
            <span class="time"> {{product.duration}}</span>
          </div>
        </div>
        <div class="price-box">
          <div class="add-cart-info"> <img src="../assets/icons/add_cart.png" class="add-cart-icon" alt="img1"></div>
          <div class="price-info">
            <div class="main-price">%{{product.price.base}}</div>
            <div class="final-price-box">
              <div class="final-price">{{product.price.final }}</div>
              <div class="price-Toman">تومان
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="box-item discount" id="discount"> <span>%{{Math.round(((product.price.base-product.price.final) /(product.price.base))*100)}} </span></div>
  </div>
</template>
<script>
export  default {
  props: ['product'],
  data(){
    return{
    }
  },
  methods:{
  }
}
</script>
<style>
.product-item-box {
  margin-bottom: 25px;
  padding: 15px;
  position: relative;
  border-radius: 20px;
  box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16);
  background-color: #ffffff;
}

.product-item-box .product-item-main-box .img-box .img {
  width: 100%;
  height: 100%;
}
/*----------------title--------------*/
.product-item-box .product-item-main-box .product-item-content .main-title {
  margin-top: 7px;
  margin-bottom: 5px;
}
.product-item-box .product-item-main-box .product-item-content .main-title .title-box{
  display: flex;
  align-items: center;
  width: 100%;
  height: 48px;
}
.product-item-box .product-item-main-box .product-item-content .main-title .title-box .title-text {
  font-size: 16px;
  font-weight: 500;
  font-stretch:normal;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  text-overflow: ellipsis;
  letter-spacing: normal;
  color: #333333;
  overflow: hidden;
}
/*--------------------author box---------------------*/
.product-item-box .product-item-main-box .product-item-content .time-author-box {
  display: flex;
  flex-wrap: nowrap;
  justify-content: space-between;
  font-size: 13px;
  margin-bottom: 10px;
}
.product-item-box .product-item-main-box .product-item-content .time-author-box .box-item .author {
  color: #666666;
}
.product-item-box .product-item-main-box .product-item-content .time-author-box .box-item .teacher-icon {
  width: 13px;
  height: 13px;
  margin-left: 6px;
}
.product-item-box .product-item-main-box .product-item-content .time-author-box .box-item .time-icon {
  width: 12px;
  height: 12px;
  margin-left: 6px;
}
.product-item-box .product-item-main-box .product-item-content .time-author-box .box-item .time {
  color: #666666;
}
.product-item-box .product-item-main-box .product-item-content .time-author-box .box-item {
  display: flex;
  justify-content: center;
  align-items: center;
}
/*-------------------price box----------------------*/
.product-item-box .product-item-main-box .product-item-content .price-box .add-cart-info {
  display: flex;
  justify-content: center;
  align-items: center;
}
.product-item-box .product-item-main-box .product-item-content .price-box .price-info {
  display: flex;
  justify-content: center;
  align-items: baseline;
}
.product-item-box .product-item-main-box .product-item-content .price-box .price-info .final-price-box {
  display: flex;
  justify-content: center;
  align-items: center;
}
.product-item-box .product-item-main-box .product-item-content .price-box {
  display: flex;
  flex-wrap: nowrap;
  justify-content: space-between;
}
.product-item-box .discount {
  width: 54px;
  height: 54px;
  border-radius: 0 20px 0 20px;
  order: -1;
  position: absolute;
  background-color: #ff5050;
  color: white;
  top: 0;
  right: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}
.product-item-box .product-item-main-box .product-item-content .price-box .price-info .main-price {
  color: #ff5050;
  text-decoration: #333333 line-through;
  font-size: 13px;
  font-weight: 500;
}
.product-item-box .product-item-main-box .product-item-content .price-box .price-Toman {
  font-size: 13px;
}
.product-item-box .product-item-main-box .product-item-content .price-box .price-info .final-price-box .final-price {
  margin-left: 6px;
  margin-right: 11px;
  font-size: 18px;
}
.product-item-box .product-item-main-box .product-item-content .price-box .add-cart-info .add-cart-icon {
  width: 19px;
  order: 1;
}


@media screen and (max-width: 768px){
  .product-item-box{
    border-radius: 10px;

  }
  .product-item-box .product-item-main-box {
    display: flex;
    flex-wrap: wrap;
    /*justify-content: space-between;*/
  }
  .product-item-box .product-item-main-box .product-item-content {
    width: calc(100% - 90px);
    padding-right: 15px;
  }
  .product-item-box .product-item-main-box .img-box .img{
    width: 90px;
    height: 90px;
  }
  .product-item-box .product-item-main-box .product-item-content .price-box {
    align-items:flex-end;
    justify-content: flex-end;
  }
  .product-item-box .product-item-main-box .product-item-content .price-box .add-cart-info {
    order: 2;
  }
  .product-item-box .product-item-main-box .product-item-content .price-box .price-info {
    flex-direction: column;
  }
  .product-item-box .product-item-main-box .product-item-content .price-box .price-info .final-price-box {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .product-item-box .product-item-main-box .product-item-content .price-box .price-box .main-price {
    font-size: 11px;
  }
  .product-item-box .product-item-main-box .product-item-content .price-box .price-info .final-price-box.final-price {
    margin-right: 0px;
    font-size: 16px;
  }
  .product-item-box .product-item-main-box .product-item-content .price-box .price-box .price-Toman {
    font-size: 11px;
  }
  .product-item-box .product-item-main-box .product-item-content .main-title .title-box .main-title .title-text {
    font-size: 14px;
  }
  .product-item-box .product-item-main-box .product-item-content .main-title{
    height: 44px;
    margin-top: 0;
    margin-bottom: 0;
    padding: 0;
  }
  .product-item-box .product-item-main-box .product-item-content .price-box .add-cart-info{
    margin-right: 30px;
  }
  .product-item-box .product-item-main-box .product-item-content .time-author-box {
    margin-bottom: 0;
  }
  .product-item-box .discount {
    border-radius: 10px 10px 0 0;
    position: absolute;
    top:auto;
    bottom:0;
    width: 45px;
    height: 35px;
    margin-right: 120px;
  }
}
@media  screen and (max-width:376px){
  .product-item-box{
    padding: 15px;
  }
  .product-item-box .product-item-main-box .img-box .img{
    width: 90px;
    height: 90px;

  }

  .product-item-box .product-item-main-box .product-item-content .time-author-box {
    font-size: 11px;
  }
  .product-item-box .product-item-main-box .product-item-content .main-title .title-box .title-text{
    font-size: 14px;
  }
  .product-item-box .product-item-main-box .product-item-content .price-box .price-info .final-price-box .final-price {
    margin-left: 6px;
    margin-right: 0;
    font-size: 16px;
  }
  .product-item-box .product-item-main-box .product-item-content .price-box  .price-info .final-price-box{
    /*margin-right: 16px;*/
  }
  .product-item-box .product-item-main-box .product-item-content .price-box .price-box .price-Toman {
    font-size: 11px;
  }
  .product-item-box .product-item-main-box .product-item-content .price-box .price-box .add-cart-info{
    margin-top: 4px;
  }
  .product-item-box .discount {
    width: 45px;
    height: 35px;
  }
  .product-item-box .product-item-main-box .product-item-content .price-box .add-cart-info {
    margin-right: 15px;
  }
}
@media screen and (max-width: 350px){

  .product-item-box .product-item-main-box .product-item-content  .product-item-content{
    padding: 0px;
  }
}
@media  screen and (max-width:300px){
  .product-item-box{
    padding: 10px;
  }
  .product-item-box .product-item-main-box .product-item-content {
    width: calc(100% - 70px);
    padding-right: 10px;
  }
  .product-item-box .product-item-main-box .img-box{

  }
  .product-item-box .product-item-main-box .img-box .img{
    width: 70px;
    height: 70px;
  }

  .product-item-box .product-item-main-box .product-item-content .price-box .price-info .main-price{
    font-size: 11px;
  }
  .product-item-box .product-item-main-box .product-item-content .price-box .price-info .final-price-box .final-price {
    margin-right: 0;
    font-size: 16px;
  }
  .product-item-box .discount {
    /*display: none;*/
    margin-right: 89px;
    margin-left: 16px;
  }

}
</style>
