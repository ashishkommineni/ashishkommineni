# Ashish Kommineni

### VLSI Design & Verification Engineer

I build specification-driven RTL and verification environments for digital interfaces and data-path blocks. My work centers on SystemVerilog, UVM, assertions, constrained-random stimulus, scoreboards, coverage closure, regressions, and waveform-led debug.

I care about the details that make verification trustworthy: independent AXI channels, AHB address/data pipelining, APB wait-state stability, open-drain I²C behavior, SPI edge selection, UART framing, and FIFO boundary conditions.

## Featured verification portfolio

| Project | Design scope | Verification focus |
|---|---|---|
| [AXI4-Lite Memory Slave](https://github.com/ashishkommineni/axi4-lite-uvm-verification) | Independent AW/W channels, byte strobes, response backpressure | UVM memory model, actual channel-skew coverage, five stable-VALID assertions |
| [AHB-Lite Memory Slave](https://github.com/ashishkommineni/ahb-lite-uvm-verification) | Pipelined address/data phases, wait states, two-cycle ERROR | Phase-aware monitor, response checking, stalled-control SVA |
| [APB3 Register Slave](https://github.com/ashishkommineni/apb3-uvm-verification) | Four-register peripheral, programmable waits, `PSLVERR` | Setup/access checks, legal and unaligned traffic, register scoreboard |
| [I²C Write Master](https://github.com/ashishkommineni/i2c-master-uvm-verification) | Open-drain single-byte writes, ACK/NACK, clock-stretch awareness | Pin-level target model, serial decode, open-drain assertions |
| [SPI Master](https://github.com/ashishkommineni/spi-master-uvm-verification) | Modes 0–3, four chip selects, full-duplex transfer | Mode × target coverage, loopback scoreboard, idle/selection SVA |
| [UART](https://github.com/ashishkommineni/uart-uvm-verification) | Configurable data bits, optional even/odd parity | End-to-end serial loopback, framing checks, payload × parity coverage |
| [Asynchronous FIFO](https://github.com/ashishkommineni/asynchronous-fifo-uvm-verification) | Gray pointers, two-flop synchronizers, unrelated clocks | Dual-agent UVM, cross-domain ordering scoreboard, CDC-aware boundaries |
| [Synchronous FIFO](https://github.com/ashishkommineni/synchronous-fifo-uvm-verification) | Parameterized depth/width, simultaneous read/write | Queue scoreboard, occupancy coverage, overflow/underflow assertions |

Every repository includes synthesizable RTL, a complete UVM environment, constrained-random and directed stimulus, a scoreboard, functional coverage, SVA, a portable self-checking smoke test, verification results, and reproducible run commands for Cadence Xcelium.

## Learning in public

I also maintain the [SystemVerilog DV Learning Lab](https://github.com/ashishkommineni/systemverilog-dv-learning-lab): nine focused chapters that move from language fundamentals and OOP to constraints, concurrency, interfaces, assertions, coverage, a mini verification project, and interview practice. Each topic is kept small enough to run, inspect, and explain—not just copy.

## How I approach a block

1. Turn the protocol or microarchitecture into an explicit behavioral contract.
2. Implement bounded, synthesizable RTL and state what is intentionally out of scope.
3. Build monitor-first checking so the scoreboard uses observed handshakes, not driver intent.
4. Add directed corner cases, then constrained-random traffic and meaningful coverage crosses.
5. Run assertions with executable smoke tests and use seeded regressions for closure.
6. Record exact PASS evidence and keep tool/sign-off limitations visible.

## Technical toolbox

| Area | Skills |
|---|---|
| Languages | SystemVerilog, Verilog, Python, C, shell scripting |
| Verification | UVM, SVA, constrained-random stimulus, scoreboards, functional/code coverage, regression debug |
| Interfaces | AMBA AXI, AHB-Lite, APB, I²C, SPI, UART |
| Digital design | RTL, FSMs, FIFOs, CDC fundamentals, setup/hold and STA fundamentals |
| Tools | Cadence Xcelium, Synopsys VCS/Verdi, QuestaSim/ModelSim, Vivado, Git |

## Experience and education

- Freelance VLSI Verification Engineer / Consultant — remote, Nov 2025–present
- VLSI Design & Verification Intern — Sumedha IT Pvt Ltd, Hyderabad, May–Oct 2025
- B.Tech, Electrical & Electronics Engineering — RVR & JC College of Engineering, Guntur, 2024; CGPA 8.02/10
- VLSI Design & Verification training — Sumedha IT

## Publication

“Design and Implementation of PI-Based TLBO MPPT Controller for Grid-Tied PV Microgrid,” *International Journal of Management, Technology and Engineering*, May 2024.

## Connect

[LinkedIn](https://www.linkedin.com/in/ashish-kommineni) · [Email](mailto:ashishkommineni7@gmail.com)
