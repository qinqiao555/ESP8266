# ESP8266

[中文](./README_zh.md) | English

ESP8266 driver supported by QuecPython

## Table of Contents

- [Introduction](#introduction)
- [Directory Structure](#Directory Structure)
- [Usage](#Usage)
- [Contributing](#contributing)
- [License](#license)
- [Support](#support)

## Introduction

ESP8266 is a low-cost, low-power system on chip that integrates a 32-bit Tensilica processor. It supports clock speeds of 80MHz and 160MHz and has efficient processing capabilities. Supports real-time operating systems (RTOS) and Wi Fi protocol stacks, allowing up to 80% of processing power to be reserved for application programming and development. ESP8266 also has rich interfaces, including UART, I2C, SPI, GPIO, etc., supporting multiple peripheral connections and data transmission.

## Directory Structure

```plaintext
ESP8266/
├── datasheet/
│   └── esp8266ex_datasheet_en.pdf
├── test/
│   └── esp8266.py
├── .gitignore
├── LICENSE
├── README.md
└── README_zh.md
```

## Usage

- After connecting the module to the ESP8266 module, import the `esp8266.py` script from the test directory into the module, and then click run.
- After successful operation, ESP8266 will generate a Wi Fi access point called `ESP8266`, which can provide wireless network connection for other devices.

```python
if __name__=="__main__":
	esp8266 = Esp8266_ap(UART.UART2)
	esp8266.set_ap(name='ESP8266',pwd='11111111')
	err = esp8266.wifi_on()
	if err == 0:
		print('slip network card create success')
	else:
		print('slip network card create fail')
```

## Contributing

We welcome contributions to improve this project! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m 'Add your feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.

## License

This project is licensed under the Apache License. See the [LICENSE](LICENSE) file for details.

## Support

If you have any questions or need support, please open an issue in this repository.