# Inline Duct Fan Controller with ESP32 and ESPHome

This project provides a comprehensive solution for controlling an inline duct fan using an ESP32 microcontroller with ESPHome, all housed on a custom-designed PCB.  The project incorporates environmental monitoring with an SCD41 CO2, temperature, and humidity sensor, and efficient power delivery with a buck converter module.

## Features

* **PWM Fan Control:** Precisely control the speed of your inline duct fan using Pulse Width Modulation (PWM) for optimal airflow and noise reduction. Compatible with a wide range of fans, including:
    * **Standard Inline Duct Fans:**  Most standard inline duct fans with PWM support.
    * **TerraBloom Fans:**  Directly compatible with TerraBloom fans via a 4-pin 3.5mm jack on the board.
    * **DucTurbo Fans:** Directly compatible with DucTurbo fans via a 4-pin 3.5mm jack on the board.
    * **AC Infinity Fans:**  Compatible with AC Infinity fans with a minor modification to the PWM circuit (a resistor smaller than 1k must be used).  See the [modification guide](link-to-modification-guide) for details. 
* **ESPHome Integration:** Seamlessly integrate the fan controller into your Home Assistant setup or any other ESPHome-compatible system.
* **Tasmota Support (Untested):** While this project primarily focuses on ESPHome, it should be possible to use Tasmota with the custom PCB. However, this has not been tested yet. Contributions and feedback regarding Tasmota compatibility are welcome!
* **Environmental Monitoring:**  Monitor CO2 levels, temperature, and humidity in your environment with the integrated SCD41 sensor, enabling automated ventilation control based on air quality and environmental conditions.
* **Custom PCB:**  A purpose-built PCB ensures a clean and professional installation, simplifying wiring and component placement.
* **Buck Converter:**  Efficiently step down voltage to power the ESP32 and other components, ensuring stable operation and minimizing heat generation.
* **Modular Design:**  The SCD41 and buck converter are included as drop-in modules, allowing for easy replacement or upgrades.

## Hardware

* **Custom PCB:** Designed specifically for this project, the PCB includes designated footprints for the ESP32, SCD41, buck converter, terminal blocks for easy wiring, and a 4-pin 3.5mm jack for connecting DucTurbo and TerraBloom fans.
* **ESP32 Dev Board:**  Provides the processing power and Wi-Fi capabilities for the project. Any ESP32 development board with sufficient GPIO pins can be used.
* **Inline Duct Fan:**  Select a fan compatible with PWM control for optimal performance.
* **SCD41 CO2 Sensor Module:**  Provides accurate CO2, temperature, and humidity measurements for environmental monitoring.
* **Buck Converter Module:**  Efficiently steps down voltage to power the ESP32 and other components.

## Software

* **ESPHome:**  Used to program and configure the ESP32, enabling easy integration with Home Assistant or other platforms.
* **YAML Configuration:**  The fan controller is configured using a simple and intuitive YAML file, allowing for customization of fan speed, CO2 thresholds, temperature and humidity setpoints, and other parameters.
* **Tasmota (Optional):**  While untested, Tasmota may be used as an alternative firmware for the ESP32.

## Assembly

1. **Solder Components:**  Solder the ESP32, buck converter, and terminal blocks to the custom PCB.
2. **Install Modules:**  Insert the SCD41 and buck converter modules into their designated footprints on the PCB.
3. **Wire Fan and Power:**  
    * For DucTurbo and TerraBloom fans, connect the fan's 4-pin 3.5mm cable to the jack on the PCB.
    * For other fans, connect the inline duct fan and power supply to the terminal blocks on the PCB.
4. **Flash ESP32:**  Use ESPHome or Tasmota to flash the ESP32 with the desired firmware.
5. **Integrate with Home Assistant (ESPHome):**  Add the ESP32 device to your Home Assistant instance and configure automations or dashboards as desired.

## Usage

Once assembled and configured, the inline duct fan controller can be operated manually or automatically based on CO2 levels, temperature, humidity, timers, or other triggers. The ESPHome integration allows for seamless control and monitoring through Home Assistant or other compatible platforms.

## Future Enhancements

* **Display:**  Add an OLED display to show real-time CO2 levels, fan speed, and other information.
* **Web Interface:**  Develop a web interface for configuration and control, accessible from any device on the network.
* **Tasmota Testing and Documentation:**  Test and document the use of Tasmota with this project.

## Contributing

Contributions to this project are welcome!  Feel free to submit bug reports, feature requests, or pull requests on the GitHub repository.  Testing and documenting Tasmota compatibility would be a valuable contribution.

