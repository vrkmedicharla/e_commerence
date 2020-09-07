<template>
    <div>
   
    <div class="row q-ma-xl">
    <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6 col-xl-6 text-center">
     <img :src="item.img" height="450px" width="450px" />
    </div>
    <div class="col-xs-12 col-sm-12 col-md-5 col-lg-5 col-xl-5 q-ma-md">
    <div class="q-py-lg" >
    <h4 class="title">
    {{item.title}} </h4>
    <span >
    Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
    </span>
    
    </div>
    <div>
    <span class="side-title">Price per unit</span></div>
    <div class="q-py-xl line">
    <strong >{{item.cost}}</strong>
    </div>
    <div class="line">
    <q-btn color="blue" label="Buy now" />  <q-icon class="q-px-md" size="sm" name="add_shopping_cart" />
    </div>
    </div>

    </div>
    </div>
</template>
<script>
export default {
     props: {
    item: {
      required: true
    },
    
  },
    data(){
        return{

        }
    }
}
</script>
