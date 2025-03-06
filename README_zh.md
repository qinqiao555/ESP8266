# ESP8266

中文 | [English](./README.md)

本仓库为 QuecPython 支持的 ESP8266 驱动程序。

## 目录

- [介绍](#介绍)
- [目录结构](#目录结构)
- [使用](#使用)
- [贡献](#贡献)
- [许可证](#许可证)
- [支持](#支持)

## 介绍

ESP8266 是一款低成本、低功耗的系统级芯片，集成了 32 位 Tensilica 处理器，主频支持 80MHz 和 160MHz，具备高效的处理能力。支持实时操作系统 (RTOS) 和 Wi-Fi 协议栈，可将高达 80% 的处理能力留给应用编程和开发。ESP8266 还具有丰富的接口，包括 UART、I2C、SPI、GPIO 等，支持多种外设连接和数据传输。

## 目录结构

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

## 使用

- 连接好模组与 ESP8266 模块后，将 test 目录下的 `esp8266.py` 脚本导入模组，然后点击运行。
- 成功运行后 ESP8266 会生成一个名为 `ESP8266` 的 Wi-Fi 接入点，可为其他设备提供无线网络连接。

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

## 贡献

我们欢迎对本项目的改进做出贡献！请按照以下步骤进行贡献：

1. Fork 此仓库。
2. 创建一个新分支（`git checkout -b feature/your-feature`）。
3. 提交您的更改（`git commit -m 'Add your feature'`）。
4. 推送到分支（`git push origin feature/your-feature`）。
5. 打开一个 Pull Request。

## 许可证

本项目使用 Apache 许可证。详细信息请参阅 [LICENSE](LICENSE) 文件。

## 支持

如果您有任何问题或需要支持，请在本仓库中打开一个 issue。