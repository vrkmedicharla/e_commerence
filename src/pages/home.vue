<template>
  <div class="">
    <q-layout >

      <q-drawer
        v-model="drawer"
        show-if-above
        :width="300"
        :breakpoint="400"
      >
      <div class="q-ma-md">
        <span>Filter by</span>
         <q-select v-model="collection" :options="collections" label="collection" />
          <q-select v-model="color" :options="colors" label="color" />
           <q-select v-model="category" :options="categories" label="category" />
           <div class="q-py-md">
           <label >Price range</label>
            <q-slider
      v-model="slider_value"
      :min="1000"
      :max="10000"
      :step="4"
        label
      label-always
      color="light-green"
    />
    <div class="row">
    <div class="col-6">$1000</div>
    
    <div class="col-6 text-right">$10000</div>
    </div>
           </div>

        </div>

     
      </q-drawer>

      <q-page-container>
        <q-page padding>
            <div class="row q-ma-md">
            <div class="col-md-4 col-sm-6 col-xs-12 col-lg-4 col-xl-4 q-pa-md" v-for="(item,i) in  items" :key="i">
            <div >
             <router-link
                  :to="{ name: 'productView', params: { item : item  }}"
                >
            <img :src="item.img" height="250px" width="250px" />
             </router-link>
            <div class="row">
            <div class="col-6 q-py-xs">{{item.title}}</div>
             <div class="col-6 q-py-xs ">${{item.cost}}</div>
             <div class="col-6 q-py-xs">
              <q-rating
      v-model="item.rating"
      max="5"
      size="xs"
      color="black"
      icon="star_border"
      icon-selected="star"
      icon-half="star_half"
      readonly
      no-dimming
    />
    </div>
     <div class="col-6 q-py-xs">
     <q-icon size="sm" name="add_shopping_cart" /></div>
            </div>
            </div>
             </div>
            </div>
                  </q-page>
      </q-page-container>
    </q-layout>
  </div>
</template>

<script>
export default {
    data(){
        return {
            drawer: false,
            collection : "",
            collections : [ 'collection-1','collection-2','collection-2'],
            color : "",
            colors : ['red','green','blue'],
            category : "",
            categories : ['categories-1','categories-2','categories-3'],
            slider_value : 4500,
            items : [
                {
                    title : "chairs" ,img : "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcQP_sseSzIaXVkgS62Pq1CMGi4TRe-DPI8U0g&usqp=CAU",
                    rating : 4, cost : 6000
                },
                {
                    title : "Interior Designer" ,img : "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcRITxH6iyg_HTiylEClbt8mhql2KSttRosj0A&usqp=CAU",
                    rating : 2, cost : 8000
                },
                {
                    title : "study chair" ,img : "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcQYDZpj2kK6fN96tjhtLFM_lRrW7swxkiLlMA&usqp=CAU",
                    rating : 3, cost : 4000
                },
                {
                    title : "chairs" ,img : "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcQP_sseSzIaXVkgS62Pq1CMGi4TRe-DPI8U0g&usqp=CAU",
                    rating : 4.5, cost : 10000
                },
                {
                    title : "Interior Designer" ,img : "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcRITxH6iyg_HTiylEClbt8mhql2KSttRosj0A&usqp=CAU",
                    rating : 3.5, cost : 8500
                },
                {
                    title : "study chair" ,img : "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcQYDZpj2kK6fN96tjhtLFM_lRrW7swxkiLlMA&usqp=CAU",
                    rating : 3, cost : 9000
                },
            ]
        }
    }
}
</script>