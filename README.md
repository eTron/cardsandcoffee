eTron's Weather Cards 

Wide and Tall use the same sensors. `eTrons-WideWeatherCard-DateConditions` uses the same sensors + 2 more for current conditions & AQI category. Also shows the date above the time.

## 📋 Prerequisites

This card is configured to use **Google Weather** and **Google AQI** for sensor data by default.

1. Navigate to **Settings > Devices & Services** in Home Assistant.
2. Click **Add Integration**.
3. Search for and install both **Google Weather** and **Google AQI**.

> **Note:** You can use other weather providers, but you **must** ensure the three (or 5 for eTrons-WideWeatherCard-DateConditions) required sensor entities (Humidity, AQI, and UV, AQI Category, Current Conditions) are correctly defined in the card variables. If these are missing, the card will display an error.

## ⚙️ Installation

### 1. Setup Icons

1. Create a folder named `weather-icons` inside your Home Assistant `www` directory (e.g., `/config/www/weather-icons`).
2. Extract the contents of the provided ZIP file into this folder.

* **Important:** Do not rename any of the files. The card relies on these specific filenames to match weather states.

### 2. Create the Card

Once the prerequisites and icons are set up, you can add the card to your dashboard.

1. Enter dashboard edit mode and **Add Card**.
2. Select **Manual**.
3. Paste the desired YAML code and **Save**.

### 3. Add this sensor to configuration.yaml under the sensors section. (you need to fix the spacing / indentation)
### sensor:
###  - platform: time_date
###    display_options:
###      - 'time'
   
⚠️ **Critical Step:** You must do the following or the time and sensor images may not appear:

1. **Restart Home Assistant** to ensure the new folder is recognized.
2. **Clear your browser cache** (and the cache of the Home Assistant Companion App if using mobile) to force the new images to load.
