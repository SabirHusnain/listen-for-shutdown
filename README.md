# pi-power-button

## Installation
- Run the setup script: `./pi-power-button/script/install`

## Uninstallation
- Run the uninstall script: `./pi-power-button/script/uninstall`

## Is it possible to use another pin other than Pin 5 (GPIO 3/SCL)?
Not for full functionality, no. There are two main features of the power button:

- **Shutdown functionality:** Shut the Pi down safely when the button is pressed. The Pi now consumes zero power.
- **Wake functionality:** Turn the Pi back on when the button is pressed again.

The **wake functionality** requires the SCL pin, Pin 5 (GPIO 3). There's simply no other pin that can "hardware" wake the Pi from a zero-power state. If you don't care about turning the Pi back _on_ using the power button, you could use a different GPIO pin for the **shutdown functionality** and still have a working shutdown button. Then, to turn the Pi back on, you'll just need to disconnect and reconnect power (or use a cord with a physical switch in it) to "wake" the Pi.