<template>
  <div>
    <city-header></city-header>
    <city-search></city-search>
    <city-list :cities="cities" :hot="hotCities"></city-list>
    <city-alphabet :cities="cities"></city-alphabet>
  </div>
</template>
<script>
import axios from 'axios'
import CityHeader from './pages/Header'
import CitySearch from './pages/Search'
import CityList from './pages/List'
import CityAlphabet from './pages/Alphabet'

export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch,
    CityList,
    CityAlphabet
  },
  data () {
    return {
      cities: {},
      hotCities: []
    }
  },
  methods: {
    getCityInfo () {
      axios.get('/api/city.json')
        .then(this.handletCityInfoSucc)
    },
    handletCityInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.cities = data.cities
        this.hotCities = data.hotCities
      }
      console.log(res)
    }
  },
  mounted () {
    this.getCityInfo()
  }
}
</script>
<style lang="stylus" scoped>

</style>
