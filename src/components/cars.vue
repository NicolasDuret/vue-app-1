<template>
  <div>
    <ul v-for='car in cars' :key=car.name>
        <li>{{  car.name  }} </li>
        <li>{{  car.model  }} </li>
        <li>{{  car.year  }} </li>
    </ul>
    <button> @click='addCar'> Add Car </button>
    <p> Nombre de voitures : {{ counter }}</p>
  </div>
</template>

<script>
export default {
    data () {
        return {
            cars: []
        }
    },
    methods: {
        addCar () {
        this.cars.push({
            'name': 'ford',
            'model': 'fiesta',
            'year': '2008'
        })
    }
  },
  computed: {
    counter () {
      return this.cars.lenght
    }
  },
  mounted: {}
  }
</script>
