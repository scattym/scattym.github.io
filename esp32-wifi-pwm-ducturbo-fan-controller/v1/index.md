# Inline Duct Fan Controller with ESP32 and ESPHome

This project provides a comprehensive solution for controlling an inline duct fan using an ESP32 microcontroller with ESPHome, all housed on a custom-designed PCB.  The project incorporates environmental monitoring with an SCD41 CO2 sensor and efficient power delivery with a buck converter module.

## Features

* **PWM Fan Control:** Precisely control the speed of your inline duct fan using Pulse Width Modulation (PWM) for optimal airflow and noise reduction.
* **ESPHome Integration:** Seamlessly integrate the fan controller into your Home Assistant setup or any other ESPHome-compatible system.
* **CO2 Monitoring:** Monitor CO2 levels in your environment with the integrated SCD41 sensor, enabling automated ventilation control based on air quality.
* **Custom PCB:**  A purpose-built PCB ensures a clean and professional installation, simplifying wiring and component placement.
* **Buck Converter:**  Efficiently step down voltage to power the ESP32 and other components, ensuring stable operation and minimizing heat generation.
* **Modular Design:**  The SCD41 and buck converter are included as drop-in modules, allowing for easy replacement or upgrades.

## Hardware

* **Custom PCB:** Designed specifically for this project, the PCB includes designated footprints for the ESP32, SCD41, buck converter, and terminal blocks for easy wiring.
* **ESP32 Dev Board:**  Provides the processing power and Wi-Fi capabilities for the project. Any ESP32 development board with sufficient GPIO pins can be used.
* **Inline Duct Fan:**  Select a fan compatible with PWM control for optimal performance.
* **SCD41 CO2 Sensor Module:**  Provides accurate CO2 measurements for environmental monitoring.
* **Buck Converter Module:**  Efficiently steps down voltage to power the ESP32 and other components.

## Software

* **ESPHome:**  Used to program and configure the ESP32, enabling easy integration with Home Assistant or other platforms.
* **YAML Configuration:**  The fan controller is configured using a simple and intuitive YAML file, allowing for customization of fan speed, CO2 thresholds, and other parameters.

## Assembly

1. **Solder Components:**  Solder the ESP32, buck converter, and terminal blocks to the custom PCB.
2. **Install Modules:**  Insert the SCD41 and buck converter modules into their designated footprints on the PCB.
3. **Wire Fan and Power:**  Connect the inline duct fan and power supply to the terminal blocks on the PCB.
4. **Flash ESP32:**  Use ESPHome to flash the ESP32 with the provided YAML configuration file.
5. **Integrate with Home Assistant:**  Add the ESP32 device to your Home Assistant instance and configure automations or dashboards as desired.

## Usage

Once assembled and configured, the inline duct fan controller can be operated manually or automatically based on CO2 levels, timers, or other triggers. The ESPHome integration allows for seamless control and monitoring through Home Assistant or other compatible platforms.

## Future Enhancements

* **Temperature and Humidity Sensing:**  Integrate a temperature and humidity sensor for more comprehensive environmental monitoring.
* **Display:**  Add an OLED display to show real-time CO2 levels, fan speed, and other information.
* **Web Interface:**  Develop a web interface for configuration and control, accessible from any device on the network.

## Contributing

Contributions to this project are welcome!  Feel free to submit bug reports, feature requests, or pull requests on the GitHub repository.
