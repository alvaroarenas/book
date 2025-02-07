# probe-rs

The probe-rs project is a set of tools to interact with embedded MCU's using various debug probes. It is similar to openOCD, PyOCD, Segger tools etc. There is support for ARM & RISCV architectures along with a collection of tools, including but not limited to:

- Debugger
  - GDB support.
  - CLI for interactive debugging.
  - VSCode extension.
- RTT (Real Time Transfer)
  - Similar to app_trace component of IDF.
- Flashing algorithms

More info about probe-rs & how to set up a project, can be found on the [probe.rs](https://probe.rs/) website.

## `USB-JTAG-SERIAL` peripheral for ESP32-C3 

Starting from `probe-rs` v0.12, it is possible to flash and debug the ESP32-C3 with the builtin `USB-JTAG-SERIAL` peripheral, no need for any external hardware debugger. More info on configuring the interface can be found in the [official documentation].

## Support for Espressif chips

`probe-rs` currently only supports ARM & RISCV, therefore this limits the number of Espressif chips that can be used at the moment.

|   Chip   |   Flashing   |   Debugging   |
| :------: | :----------: | :-----------: |
| ESP32-C3 |      ✅      |       ⚠️      |

**Note**: _items marked with ⚠️ are currently work in progress, usable but expect bugs._

[official documentation]: https://docs.espressif.com/projects/esp-idf/en/latest/esp32c3/api-guides/jtag-debugging/configure-builtin-jtag.html

<!-- TODO: when probe-rs can actually debug at least a C3 with decent back traces etc, add a section here with an example config: see https://github.com/probe-rs/probe-rs/issues/877 -->