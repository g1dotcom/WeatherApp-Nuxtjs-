<template>
  <div>
    <h1>Weather App</h1>
    <input type="text" v-model="city" />
    <button @click="getWeatherInfo">Get Weather</button>
    <div v-if="weather.weather">
      <h2>{{ weather.name }}</h2>
      <p>{{ weather.weather[0].description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      city: "London",
      weather: {},
    };
  },

  created() {
    this.getWeatherInfo();
  },

  methods: {
    getWeatherInfo() {
      fetch(
        `https://api.openweathermap.org/data/2.5/weather?q=${this.city}&appid=3320da48438dec85f7460ff6068efb7b`
      )
        .then((response) => response.json())
        .then((weather) => {
          this.weather = weather;
        });
    },
  },
};
</script>
