# ESP32 HTTP Client

A simple HTTP Client example that connects to http://example.org and prints the response to the serial port.

Includes an [automated test scenario](./http-client.test.yaml) that runs the simulation and validates the serial output.

Use [Wokwi](https://marketplace.visualstudio.com/items?itemName=wokwi.wokwi-vscode) to simulate this project, and the [Wokwi CLI](https://github.com/wokwi/wokwi-cli) to run the automated test.

## Building

This is a [PlatformIO](https://platformio.org) project. To build it, [install PlatformIO](https://docs.platformio.org/en/latest/core/installation/index.html), and then run the following command:

```
pio run
```

## Simulate the project

To simulate this project, install [Wokwi for VS Code](https://marketplace.visualstudio.com/items?itemName=wokwi.wokwi-vscode). Open the project directory in Visual Studio Code, press **F1** and select "Wokwi: Start Simulator".

## Run in wokwi-cli

To run the automated test scenario, install the [Wokwi CLI](https://github.com/wokwi/wokwi-cli/#installation), and create a [Wokwi CLI token](https://wokwi.com/dashboard/ci). Then run the following commands:

Linux/Mac:

```bash
export WOKWI_CLI_TOKEN="your token goes here"
wokwi-cli --scenario http-client.test.yaml .
```

Windows:

```powershell
$env:WOKWI_CLI_TOKEN="your token goes here"
wokwi-cli --scenario http-client.test.yaml .
```
