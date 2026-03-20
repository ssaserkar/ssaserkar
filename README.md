# Soham Aserkar

I validate the power stages that feed AI processors at [Renesas Electronics](https://www.renesas.com/), and I build software that measures what those processors actually consume.

Most hardware engineers don't write software. Most software engineers don't understand hardware. I do both — specifically where power delivery meets AI compute.

## What I'm Working On

**[PowerLens](https://github.com/ssaserkar/powerlens)** — I built an open-source tool that measures the real energy cost of AI inference on NVIDIA Jetson. It reads the hardware power sensors (INA3221 via sysfs), correlates power with individual inferences, and reports joules per inference — something tegrastats and jtop can't do.

Results from real hardware (Jetson Orin Nano):
- Small model: 0.010 J/inference at 13.6W
- Large model: 1.281 J/inference at 35.3W — 128x more energy
- 25W power mode is more efficient than max performance mode
- GPU temperature rises 10°C under sustained 150-second load

63 tests. 7 CLI commands. Validated against tegrastats within 2%.

## Background

- **Application Engineer** — [Renesas Electronics](https://www.renesas.com/) — Power stage validation, multiphase DC-DC controllers, VRM characterization
- **Graduate Research** — [WPI](https://wp.wpi.edu/smerl/) — Published research on AI-driven policy analysis (LSTM/ESN with attention, F1=0.79)
- **Hardware Validation** — [Eaton](http://www.eaton.in/) — HIL/PIL/SIL verification
- **Electronics Design** — [IUCAA / LIGO](https://www.iucaa.in/) — Gravitational wave detector electronics

**MS Robotics** — Worcester Polytechnic Institute

## Open to Collaboration

I'm interested in open-source projects where power hardware meets software — edge AI energy measurement, server power management, BMC firmware, hardware telemetry.

If you're working on something in this space and want to collaborate, or if you're using PowerLens and run into problems, open an issue or reach out directly.

## Contact

**soham339@gmail.com**
