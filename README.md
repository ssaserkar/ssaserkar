# Soham Aserkar

I validate the power stages that feed AI processors at [Renesas Electronics](https://www.renesas.com/), and I build software that measures what those processors actually consume.

Most hardware engineers don't write software. Most software engineers don't understand hardware. I do both — specifically where power delivery meets AI compute.

## What I'm Working On

**[PowerLens](https://github.com/ssaserkar/powerlens)** — I built an open-source tool that measures the real energy cost of AI inference on NVIDIA Jetson. It reads the hardware power sensors (INA3221 via sysfs), correlates power with individual inferences, and reports millijoules per inference — something tegrastats and jtop can't do.

Results from real hardware (Jetson Orin Nano, 5 models, 3 power modes, FP16 TensorRT):
- MobileNetV2: 10.3 mJ/inference — ResNet-50: 22.6 mJ/inference (2.2× more energy)
- 25W mode is universally optimal — best energy efficiency across all five models tested
- Latency varies less than 2% across power modes — you get efficiency for free
- SoC static power is 34–44% of compute — nearly half the energy keeps the chip alive, not your model
- FP16 saves 1.1–2.1× energy over FP32 depending on model architecture
- Batch size 8 is 2× more efficient than batch size 1
- Thermal steady state at 67.5°C with 18°C headroom under 600-second sustained max load — no throttling

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
