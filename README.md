# raspberry-hmi

An HMI that runs on Linux with Chromium kiosk mode and communicates with a PLC.
It uses a layers architecture, where each layer can be configured separately. 

## Communication Layer

This layer can be configured to use OPCUA, ModBusTCP, HTTP, and more coming in the future.
An Endpoint is needed and security settings, like username and password or certificates.

## Widgets Layer

Here you define which widgets you want to use and what data they should read, write or subscribe to. You can configure each widget separately. It supports custom widgets, so you can also create your own widgets using react and add them to your UI, there are no boundaries. Each widget takes its own dependencies, so you could even use threeJS to show a 3D Model of your machine in a widget. 

Available Widgets:

- Username/password authentication
- Line graph
- Pie chart
- Toggle Button
- Button
- Radio Button
- Check Button
- Text Input
- Slider
- Text
- more coming

## UI Layer

This layer is responsible for showing the widgets, each widget will be placed where you defined in the Widgets Layer.

Run an Web interface in kiosk mode with a local NodeJS server that comunicates over OPC UA with any OPC UA enabled device.
