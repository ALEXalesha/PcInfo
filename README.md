# PcInfo

**Planned.** A Windows utility that shows what is inside the PC: graphics card, processor, memory sticks and
their speed, disks with SMART, motherboard, monitors and Windows; temperatures and load as live charts with an
overheat warning; USB devices and open network ports with the program that holds each one.

[Русская версия](README.ru.md)

## Status

There is no code yet. The plan was agreed on 23.10.2026 and the work is queued. This README describes the plan,
not a working program.

## What it will show

| Block | What |
|---|---|
| Hardware | GPU, CPU, memory (sticks, speed, timings where Windows reports them), disks and SMART, motherboard, monitors, Windows version |
| Sensors | Temperatures, clocks, fans and load as live charts; a warning when something overheats |
| Ports and devices | USB devices, network ports that are open and which program listens on each |
| Quick tests | Memory bandwidth and a short check of its own buffer (not a full memtest), disk speed with a temporary file that is deleted afterwards |

A "my PC" report can be saved without serial numbers, MAC addresses, UUIDs or user and computer names.

## How it will work

- C# .NET 8 WPF, the same themes as Paint Pro, LibreHardwareMonitorLib and WMI for the data.
- Some sensors need administrator rights and a sensor driver; without them the app says what is missing instead of
  failing.

## License

MIT, see [LICENSE](LICENSE).
