# current-weather-data

npm module to get current weather at a given location, using the API from yr.no.

## Install

> $ npm install current-weather-data

## Usage

```js
const getWeather = require('current-weather-data')

const location = {
    lat: 57.123456,
    lon: 11.543212
}

getWeather(location)
    .then(weather => {
        console.log(`The temperature here is ${weather.temperature.value}`)
    })
```

## Weather data

The returned weather data looks something like this, and is a direct translation from the yr.no XML response.

```json
{
      "altitude": "131",
      "latitude": "58",
      "longitude": "12",
      "temperature": {
        "id": "TTT",
        "unit": "celsius",
        "value": "5.3"
      },
      "windDirection": {
        "id": "dd",
        "deg": "193.2",
        "name": "S"
      },
      "windSpeed": {
        "id": "ff",
        "mps": "8.7",
        "beaufort": "5",
        "name": "Frisk bris"
      },
      "windGust": {
        "id": "ff_gust",
        "mps": "18.4"
      },
      "humidity": {
        "unit": "percent",
        "value": "94.3"
      },
      "pressure": {
        "id": "pr",
        "unit": "hPa",
        "value": "995.7"
      },
      "cloudiness": {
        "id": "NN",
        "percent": "100.0"
      },
      "fog": {
        "id": "FOG",
        "percent": "0.0"
      },
      "lowClouds": {
        "id": "LOW",
        "percent": "99.8"
      },
      "mediumClouds": {
        "id": "MEDIUM",
        "percent": "79.6"
      },
      "highClouds": {
        "id": "HIGH",
        "percent": "100.0"
      },
      "dewpointTemperature": {
        "id": "TD",
        "unit": "celsius",
        "value": "4.4"
      }
    }
```
