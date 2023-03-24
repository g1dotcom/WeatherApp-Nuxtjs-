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
              <p>
                <svg
                  class="icons"
                  viewBox="0 0 64 64"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <defs>
                    <style>
                      .cls-1 {
                        fill: #f1f9ff;
                      }
                      .cls-2 {
                        fill: #ff5174;
                      }
                      .cls-3 {
                        fill: #ff4869;
                      }
                      .cls-4 {
                        fill: #ffef3f;
                      }
                      .cls-5 {
                        fill: #465e85;
                      }
                    </style>
                  </defs>
                  <g id="Temperature">
                    <path
                      class="cls-1"
                      d="M18,4a6.13,6.13,0,0,0-6.14,6.14V32.3a1.87,1.87,0,0,1-.94,1.63,14,14,0,1,0,14.17,0,1.89,1.89,0,0,1-.94-1.63c0-4.64,0-22.16,0-22.16A6.13,6.13,0,0,0,18,4Z"
                    />
                    <path
                      class="cls-2"
                      d="M18,7.91a2.18,2.18,0,0,0-2.18,2.18V35.54a.89.89,0,0,1-.66.86,10,10,0,1,0,5.68,0,.9.9,0,0,1-.65-.86c0-4.12,0-25.45,0-25.45A2.18,2.18,0,0,0,18,7.91Z"
                    />
                    <path
                      class="cls-3"
                      d="M23.58,45.93A5.58,5.58,0,1,1,18,40.36,5.58,5.58,0,0,1,23.58,45.93Z"
                    />
                    <path
                      class="cls-4"
                      d="M50.18,22.1a6.24,6.24,0,1,1-6.24-6.24A6.24,6.24,0,0,1,50.18,22.1Z"
                    />
                    <path
                      class="cls-4"
                      d="M43.94,6a1.43,1.43,0,0,1,1.43,1.43V11a1.43,1.43,0,0,1-2.86,0V7.46A1.43,1.43,0,0,1,43.94,6Z"
                    />
                    <path
                      class="cls-4"
                      d="M43.94,31.77a1.43,1.43,0,0,1,1.43,1.43v3.53a1.43,1.43,0,0,1-2.86,0V33.2A1.43,1.43,0,0,1,43.94,31.77Z"
                    />
                    <path
                      class="cls-4"
                      d="M60,22.1a1.43,1.43,0,0,1-1.43,1.43H55a1.43,1.43,0,0,1,0-2.86h3.53A1.42,1.42,0,0,1,60,22.1Z"
                    />
                    <path
                      class="cls-4"
                      d="M34.26,22.1a1.42,1.42,0,0,1-1.42,1.43H29.31a1.43,1.43,0,1,1,0-2.86h3.53A1.41,1.41,0,0,1,34.26,22.1Z"
                    />
                    <path
                      class="cls-4"
                      d="M55.3,10.74a1.42,1.42,0,0,1,0,2l-2.5,2.5a1.43,1.43,0,1,1-2-2l2.49-2.49A1.44,1.44,0,0,1,55.3,10.74Z"
                    />
                    <path
                      class="cls-4"
                      d="M37.1,28.94a1.42,1.42,0,0,1,0,2l-2.5,2.49a1.43,1.43,0,0,1-2-2l2.5-2.49A1.42,1.42,0,0,1,37.1,28.94Z"
                    />
                    <path
                      class="cls-4"
                      d="M55.3,33.45a1.44,1.44,0,0,1-2,0L50.78,31a1.43,1.43,0,0,1,2-2l2.5,2.49A1.42,1.42,0,0,1,55.3,33.45Z"
                    />
                    <path
                      class="cls-4"
                      d="M37.1,15.26a1.42,1.42,0,0,1-2,0l-2.5-2.5a1.43,1.43,0,0,1,2-2l2.5,2.49A1.44,1.44,0,0,1,37.1,15.26Z"
                    />
                    <path
                      class="cls-5"
                      d="M24.14,10.43v2H20.7a1,1,0,1,1,0-2Zm0,6.05v2H20.7a1,1,0,0,1,0-2Zm0,6v2H20.7a1,1,0,0,1,0-2Zm0,6v2H20.7a1,1,0,0,1,0-2Z"
                    />
                  </g>
                </svg>

                Temperature: {{ weather.main.temp }} °C
              </p>
              <p>
                <svg
                  class="icons"
                  data-name="Layer 1"
                  id="Layer_1"
                  viewBox="0 0 64 64"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <defs>
                    <style>
                      .cls-1 {
                        fill: #0baeff;
                      }
                      .cls-2 {
                        fill: #e0e0e0;
                      }
                      .cls-3 {
                        fill: none;
                        stroke: #e0e0e0;
                        stroke-linecap: round;
                        stroke-linejoin: round;
                        stroke-width: 2px;
                      }
                    </style>
                  </defs>
                  <title />
                  <path
                    class="cls-1"
                    d="M50,38.36a18.5,18.5,0,0,1-37,0C13,22.17,28,7.14,31.5,7.14S50,22.17,50,38.36Z"
                  />
                  <path
                    class="cls-2"
                    d="M29.3,34.07c0,3.32-2.1,5.05-4.4,5.05s-4.32-1.81-4.32-4.79,1.73-5,4.44-5S29.3,31.36,29.3,34.07Zm-6,.17c0,1.66.56,2.86,1.64,2.86s1.56-1.07,1.56-2.86c0-1.61-.44-2.86-1.59-2.86S23.34,32.66,23.34,34.24ZM43,40.67c0,3.32-2.1,5.05-4.4,5.05s-4.3-1.81-4.32-4.79,1.73-5,4.44-5S43,38,43,40.67Zm-5.93.17c0,1.66.54,2.86,1.61,2.86s1.56-1.07,1.56-2.86c0-1.61-.42-2.86-1.56-2.86S37.11,39.25,37.11,40.84Z"
                  />
                  <line
                    class="cls-3"
                    x1="36.7"
                    x2="27.45"
                    y1="29.69"
                    y2="44.72"
                  />
                </svg>
                Humidity: {{ weather.main.humidity }}%
              </p>
            </div>
            <div v-if="weather.weather">
              <p>
                <svg
                  class="icons"
                  enable-background="new 0 0 128 128"
                  version="1.1"
                  viewBox="0 0 128 128"
                  xml:space="preserve"
                  xmlns="http://www.w3.org/2000/svg"
                  xmlns:xlink="http://www.w3.org/1999/xlink"
                >
                  <g id="Layer_1">
                    <rect
                      fill="#F4F5F5"
                      height="1520"
                      opacity="0"
                      width="727.938"
                      x="-379.984"
                      y="-731"
                    />
                  </g>
                  <g id="Layer_2">
                    <g>
                      <circle cx="64" cy="64" fill="#007DB9" r="64" />
                      <g>
                        <defs>
                          <circle cx="64" cy="64" id="SVGID_85_" r="64" />
                        </defs>
                        <clipPath id="SVGID_2_">
                          <use overflow="visible" xlink:href="#SVGID_85_" />
                        </clipPath>
                        <polygon
                          clip-path="url(#SVGID_2_)"
                          fill="#0071B1"
                          points="94.898,43.704 128,76.563 128,128 57.735,128 22.193,92.504    "
                        />
                        <polygon
                          clip-path="url(#SVGID_2_)"
                          fill="#006DAD"
                          points="106.318,67 128,88.555 128,128 57.735,128 22.193,92.504    "
                        />
                      </g>
                      <circle
                        cx="47.36"
                        cy="46.722"
                        fill="#FFCC07"
                        r="25.167"
                      />
                      <circle
                        cx="47.36"
                        cy="46.722"
                        fill="#F4EC4E"
                        r="17.182"
                      />
                      <circle cx="47.36" cy="46.722" fill="#F5ECDF" r="8.682" />
                      <path
                        d="M97.633,62.205c0.681-2.096,1.061-4.327,1.061-6.65c0-11.874-9.626-21.5-21.5-21.5    c-9.046,0-16.772,5.593-19.947,13.504c-2.813-1.787-6.14-2.837-9.72-2.837c-10.009,0-18.124,8.095-18.163,18.095    c-6.995,2.527-12.169,9.205-12.169,17.071c0,9.967,7.805,18.05,17.805,18.157V98h58.527c10.033,0,18.167-8.106,18.167-18.139    C111.693,71.242,105.685,64.069,97.633,62.205z"
                        fill="#6AC5F0"
                      />
                      <path
                        d="M57.247,47.559c-2.813-1.787-6.14-2.837-9.72-2.837c-10.009,0-18.124,8.095-18.163,18.095    c-6.995,2.527-12.169,9.205-12.169,17.071c0,3.964,1.25,7.618,3.366,10.603c-0.942-2.244-1.469-4.714-1.469-7.314    c0-8.001,5.499-14.795,12.624-17.365c0.04-10.172,8.306-18.407,18.502-18.407c3.646,0,7.036,1.068,9.901,2.886    c3.234-8.047,11.104-13.736,20.319-13.736c4.056,0,7.851,1.105,11.109,3.024c-3.808-3.423-8.828-5.524-14.352-5.524    C68.148,34.055,60.421,39.648,57.247,47.559z"
                        fill="#A8DBEE"
                      />
                      <path
                        d="M73.519,67.819c-1.978-1.257-4.317-1.995-6.834-1.995c-7.037,0-12.742,5.691-12.77,12.722    c-4.918,1.776-8.556,6.472-8.556,12.002c0,2.787,0.879,5.356,2.366,7.454c-0.662-1.577-1.033-3.314-1.033-5.142    c0-5.625,3.866-10.402,8.876-12.209c0.028-7.152,5.84-12.941,13.008-12.941c2.564,0,4.947,0.751,6.961,2.029    c2.274-5.657,7.807-9.657,14.285-9.657c2.851,0,5.52,0.777,7.81,2.126c-2.677-2.407-6.207-3.884-10.09-3.884    C81.183,58.326,75.751,62.258,73.519,67.819z"
                        fill="#A8DBEE"
                      />
                    </g>
                  </g>
                </svg>
                Weather: {{ weather.weather[0].main }}
                <img
                  :src="`http://openweathermap.org/img/w/${weather.weather[0].icon}.png`"
                  alt="weather icon"
                />
              </p>

              <p>
                <svg
                  class="icons"
                  viewBox="0 0 57.587 57.587"
                  width="20.315mm"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <title />
                  <g>
                    <circle cx="24.791" cy="22.025" fill="#f5ce42" r="14.185" />
                    <path
                      d="M35.272,41.063A12.292,12.292,0,1,0,23.46,25.4a8.582,8.582,0,1,0-4.854,15.659Z"
                      fill="#b9d8e8"
                    />
                    <g>
                      <path
                        d="M35.233,44.118V37.056"
                        fill="none"
                        stroke="#83b3cb"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="4"
                      />
                      <path
                        d="M24.071,49.747V45.725"
                        fill="none"
                        stroke="#9fa6b7"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="4"
                      />
                      <path
                        d="M19.617,40.9V37.056"
                        fill="none"
                        stroke="#615c9a"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="4"
                      />
                      <line
                        fill="none"
                        stroke="#9fa6b7"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="4"
                        x1="28.271"
                        x2="28.271"
                        y1="39.362"
                        y2="37.056"
                      />
                    </g>
                  </g>
                </svg>
                Description: {{ weather.weather[0].description }}
              </p>
              <div class="esimate" v-if="weather.weather">
                <h1 class="esimate">
                  Yarın {{ weather.name }} {{ esimateWeather() }}
                </h1>
              </div>
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
      weather: {
        main: {
          temp: 0,
        },
      },
    };
  },

  created() {
    this.getWeatherInfo();
    this.esimateWeather();
  },

  methods: {
    getWeatherInfo() {
      fetch(
        `https://api.openweathermap.org/data/2.5/weather?q=${this.city}&appid=3320da48438dec85f7460ff6068efb7b`
      )
        .then((response) => response.json())
        .then((weather) => {
          this.weather = weather;
          this.weather.main.temp = Math.round(this.weather.main.temp - 273.15);
        })
        .catch((error) => {
          if (this.city == "") {
            alert("Lütfen şehir adı giriniz");
          } else {
            alert("Lütfen geçerli bir şehir adı giriniz");
          }
        });
    },
    esimateWeather() {
      if (this.weather.main.temp > 30) {
        return "Çok sıcak(Ortalama 30°C üzerinde)";
      } else if (this.weather.main.temp > 20) {
        return "Ilık(Ortalama 30°C ile 20°C arasında)";
      } else if (this.weather.main.temp > 10) {
        return "Serin(Ortalama 20°C ile 10°C arasında)";
      } else {
        return "Çok soğuk(Ortalama 10°C altında)";
      }
    },
  },
};
</script>
