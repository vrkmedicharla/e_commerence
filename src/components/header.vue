<template>
  <div class="">
    <q-toolbar class="bg-secondary text-white shadow-2">
      <q-btn flat round dense icon="menu" class="q-mr-sm" />
        <q-btn class="q-px-sm"  flat dense label="Home" />
        <q-btn class="q-px-sm"  flat dense label="Shop" />
        <q-btn class="q-px-sm"  flat dense label="Magazine" />

      <q-space />
          <q-input v-model="searchItem"  >
          <template v-slot:append>
          <q-icon name="search" color="black" />
        </template>
          </q-input>
        <q-btn class="q-px-sm"  flat dense  icon="add_shopping_cart" />
        <q-btn class="q-px-sm"  flat dense label="login" />
      
    </q-toolbar>
  </div>
</template>
<script>
export default {
    data(){
        return {
            searchItem : ""
        }
    }
}
</script>