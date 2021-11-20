<template>
  <main v-if="!this.loading">
    <data-title :text="title" :dataDate="dataDate"/>

    <data-boxes :stats="stats"/>

    <country-select @get-country="getCountryData" :countries="countries"/>
  </main>
  <main class="flex flex-col align-center justify-center text-center" v-else>
      <div class="text-gray-500 text-3xl mt-10 mb-6">
        Fetching Data
      </div>
  </main>
</template>

<script>
import DataTitle from '../components/DataTitle.vue'
import DataBoxes from '../components/DataBoxes.vue'
import CountrySelect from '../components/CountrySelect.vue'

export default {
  name: 'Home',
  components: { DataTitle, DataBoxes, CountrySelect },
  data() {
    return {
      loading: true,
      title: 'Global',
      dataDate: '',
      stats: {},
      countries: {},
    }
  },
  methods: {
    async fetchedCovidData() {
      const res = await fetch('https://api.covid19api.com/summary')
      const data = await res.json()
      return data
    },
    getCountryData(country) {
      this.stats = country
      this.title = country.Country
    }
  },
  async created() {
    const data = await this.fetchedCovidData()
    this.dataDate = data.Date;
    this.stats = data.Global;
    this.countries = data.Countries;
    this.loading = false
  }
}
</script>
