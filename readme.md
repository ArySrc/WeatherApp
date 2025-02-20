# WeatherApp by AryCodes

WeatherApp is a sleek, user-friendly web application developed by **AryCodes** that provides real-time weather updates for any city worldwide. Built with HTML, CSS, and JavaScript, it leverages the OpenWeatherMap API to deliver accurate temperature, humidity, wind speed, and weather conditions with dynamic icons and smooth animations.

## Features

- **City Search**: Enter a city name to get real-time weather details.
- **Weather Data**: Displays temperature (Celsius), humidity, wind speed, and a weather description.
- **Dynamic Icons**: Changes based on weather conditions using OpenWeatherMap icons.
- **Error Handling**: Notifies users if the city is not found or input is invalid.
- **Loading Animation**: Shows a spinner while fetching data.
- **Responsive UI**: Works seamlessly on desktops, tablets, and smartphones.
- **Smooth Animations**: Enhances user experience with fade-in effects.

## How It Works

### 1. User Input
- Users type a city name in the search bar and press **Enter** or click the search button.
- The app captures this input and initiates a request.

### 2. API Request
- The `getWeather()` function makes an asynchronous `fetch` request to OpenWeatherMap:
  ```
  https://api.openweathermap.org/data/2.5/weather?q=${city}&appid=${API_KEY}&units=metric
  ```
- The API key authenticates the request, ensuring accurate data retrieval.

### 3. Data Processing
- If successful, the API response is parsed to extract:
  - City name & country
  - Temperature
  - Weather description
  - Humidity & wind speed
  - Weather icon code
- If an error occurs, a message is displayed to the user.

### 4. UI Update
- The `displayWeather()` function updates the app’s UI with the fetched weather details.
- Weather icons are loaded dynamically from OpenWeatherMap.
- The weather info smoothly fades in using CSS animations.

## Setup & Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/AryCodes/weatherapp.git
   ```
2. **Navigate to the Project Directory**:
   ```bash
   cd weatherapp
   ```
3. **Run the App**:
   Open `index.html` in a browser:
   ```bash
   open index.html  # macOS
   start index.html # Windows
   ```
4. **Configure API Key**:
   - Get an API key from [OpenWeatherMap](https://openweathermap.org/).
   - Replace the placeholder in `index.html`:
     ```javascript
     const API_KEY = 'your-api-key-here';
     ```

## Usage

- Open the app and enter a city name (e.g., "London").
- Click the search button or press **Enter**.
- The app fetches and displays the weather details.
- If the city is not found, an error message appears.
- A loading spinner indicates data is being retrieved.

## Project Structure

```
weatherapp/
├── index.html  # Main HTML, CSS, and JavaScript logic
└── README.md   # Documentation
```

## Customization

- **Units**: Change `units=metric` to `units=imperial` for Fahrenheit.
- **Styling**: Modify CSS styles to change the look and feel.
- **Additional Data**: Extend `displayWeather()` to show pressure, sunrise time, etc.

## Limitations

- Requires an active internet connection and a valid API key.
- No offline mode; data is fetched every time.
- Only supports single-city lookup.

## License

This project is open-source under the **MIT License**.

## Contact & Support

For queries, contributions, or collaborations, reach out to **AryCodes**:

- **GitHub**: [https://github.com/AryCodes](https://github.com/AryCodes)
- **Email**: [arycodes.in@gmail.com](mailto:arycodes.in@gmail.com)

## Acknowledgments

- **[OpenWeatherMap](https://openweathermap.org/)** for the API.
- **[Google Fonts](https://fonts.google.com/)** for typography support.


