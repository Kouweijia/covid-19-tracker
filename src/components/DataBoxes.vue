<template>
  <div class="grid md:grid-cols-3 gap-4">
    <div class="shadow-md bg-blue-100 p-10 text-center rounded">
      <h3 class="text-3xl text-blue-900 font-bold mb-4">cases</h3>
      <div class="text-2xl mb-4">
        <span class="font-bold">NewConfirmed:  </span>{{ numberWithCommas(stats.NewConfirmed) }}
      </div>
      <div class="text-2xl mb-4">
        <span class="font-bold">TotalConfirmed:  </span>{{ numberWithCommas(stats.TotalConfirmed) }} 
      </div>
    </div>
    <div class="shadow-md bg-blue-100 p-10 text-center rounded">
      <h3 class="text-3xl text-blue-900 font-bold mb-4">cases</h3>
      <div class="text-2xl mb-4">
        <span class="font-bold">NewDeaths:  </span>{{ numberWithCommas(stats.NewDeaths) }}
      </div>
      <div class="text-2xl mb-4">
        <span class="font-bold">TotalDeaths:  </span>{{ numberWithCommas(stats.TotalDeaths) }}
      </div>
    </div>
    <div class="shadow-md bg-blue-100 p-10 text-center rounded">
      <h3 class="text-3xl text-blue-900 font-bold mb-4">cases</h3>
      <div class="text-2xl mb-4">
        <span class="font-bold">NewRecovered:  </span>{{ numberWithCommas(stats.NewRecovered) }}
      </div>
      <div class="text-2xl mb-4">
        <span class="font-bold">TotalRecovered：</span>{{ numberWithCommas(stats.TotalRecovered) }}
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "DataBoxes",
  props: ["stats"],
  methods:{
      numberWithCommas(x){
          return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g,',')
      }
  }
};
</script>