<template>
  <div class="wrapper">
    <div class="container main">
      <div class="row">
        <div class="col-md-8 side-image" v-if="weather.weather">
          <div class="text">
            <h2 class="text-center">
              {{ weather.name }}
            </h2>
            <div v-if="weather.main">
              <p>Temperature: {{ weather.main.temp }} °C</p>
              <p>Humidity: {{ weather.main.humidity }}%</p>
            </div>
            <div v-if="weather.weather">
              <p>
                Weather: {{ weather.weather[0].main }}
                <img
                  :src="`http://openweathermap.org/img/w/${weather.weather[0].icon}.png`"
                  alt="weather icon"
                />
              </p>
              <p>Description: {{ weather.weather[0].description }}</p>
            </div>
          </div>
        </div>

        <div class="col-md-4 right">
          <form class="input-box" @submit.prevent="getWeatherInfo">
            <header>Weather App</header>
            <div class="input-field">
              <input class="input" type="text" v-model="city" required />
              <label>City Name</label>
            </div>

            <div class="input-field">
              <input type="submit" class="submit" />
            </div>
            <div class="signin"></div>
          </form>
        </div>
      </div>
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
