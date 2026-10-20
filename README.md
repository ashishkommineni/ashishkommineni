# Ashish Kommineni

### M.Tech VLSI | RTL Design & Design Verification

Hi, I’m Ashish. I am pursuing an M.Tech with a VLSI focus at Amrita Vishwa
Vidyapeetham, Coimbatore. I enjoy the point where a written requirement becomes
cycle-accurate RTL—and where verification has to prove that the behavior still
holds under reset, stalls, errors, boundary values, and awkward timing.

I use this profile as a working engineering notebook. My repositories include
the specification, RTL, testbench, assertions, coverage intent, run commands,
expected output, and a clear record of what was actually executed. I keep
simulator evidence separate from planned work instead of treating compilation
or an unexecuted command as proof.

## Selected work

| Project | Engineering focus | Verification evidence |
|---|---|---|
| [RISC-V Reliable Edge Sensor Hub SoC](https://github.com/ashishkommineni/riscv-edge-sensor-hub-soc) | SPI sensor CDC, DMA, SECDED SRAM, signed INT8 acceleration, interrupts, firmware, and UART evidence | Independent firmware/ECC model, self-checking end-to-end RTL, SVA, contention test, UVM source, waveform artifacts, and green Verilator CI |
| [RV32I Core from Scratch](https://github.com/ashishkommineni/rv32i-core-from-scratch) | Original multicycle RV32I implementation with backpressured instruction/data buses and precise terminal faults | 261-word full base-integer program, eight directed trap tests, retirement scoreboard, SVA, coverage, UVM source, and green Verilator CI |
| [14 Days of RTL](https://github.com/ashishkommineni/14-days-of-rtl) | Fourteen synthesizable blocks covering arbitration, flow control, CDC, ECC, clock gating, prediction, streaming conversion, and DMA | Self-checking testbenches, SVA, coverage gates, a [completion matrix](https://github.com/ashishkommineni/14-days-of-rtl/blob/main/docs/completion_matrix.md), and a [dated 14/14 regression report](https://github.com/ashishkommineni/14-days-of-rtl/blob/main/docs/verification_report.md) |
| [AXI4-Lite Memory Slave](https://github.com/ashishkommineni/axi4-lite-uvm-verification) | Independent AW/W acceptance, byte strobes, decode responses, and channel backpressure | Reusable UVM agent, monitor-reconstructed transfers, byte-aware scoreboard, channel-skew coverage, stable-VALID assertions, and recorded smoke results |
| [Asynchronous FIFO](https://github.com/ashishkommineni/asynchronous-fifo-uvm-verification) | Gray-coded pointers, two-flop synchronizers, and unrelated read/write clocks | Dual UVM agents, ordering scoreboard, boundary assertions, reset/error scenarios, and documented CDC limitations |
| [VLSI Interview Preparation](https://github.com/ashishkommineni/vlsi-interview-preparation) | Fourteen focused study days spanning Digital, RTL, SystemVerilog, UVM, SVA, protocols, CDC, and FIFOs | 140 reviewed questions with detailed answers, examples, common traps, and natural spoken-answer versions |

These are the projects I would start with in a technical discussion. Together
they show system integration, CPU microarchitecture, RTL reasoning, protocol
behavior, clock-domain crossing, reusable verification structure, debugging,
and reproducible evidence.

## Protocol and IP verification

| Repository | Main focus |
|---|---|
| [AHB-Lite Memory Slave](https://github.com/ashishkommineni/ahb-lite-uvm-verification) | Pipelined address/data phases, wait states, and the two-cycle ERROR response |
| [APB3 Register Slave](https://github.com/ashishkommineni/apb3-uvm-verification) | Setup/access timing, programmable waits, register prediction, and `PSLVERR` |
| [I²C Write Master](https://github.com/ashishkommineni/i2c-master-uvm-verification) | Open-drain signaling, ACK/NACK, pin-level decoding, and clock-stretch awareness |
| [SPI Master](https://github.com/ashishkommineni/spi-master-uvm-verification) | Modes 0–3, sampling/shift edges, chip-select behavior, and full-duplex transfer |
| [UART](https://github.com/ashishkommineni/uart-uvm-verification) | Word length, parity, framing, baud timing, and serial end-to-end checking |
| [Synchronous FIFO](https://github.com/ashishkommineni/synchronous-fifo-uvm-verification) | Occupancy boundaries, simultaneous operations, ordering, overflow, and underflow |

The AXI4-Lite and asynchronous-FIFO repositories are highlighted above. Across
all eight protocol/FIFO projects, the common structure includes synthesizable
RTL, UVM components, constrained stimulus, SVA, functional coverage, a
self-checking portable smoke test, verification documentation, and MIT licensing.
The latest `main`-branch portable smoke workflow is green in each repository;
those runs check RTL/SVA portability and do not claim a full Xcelium UVM run.

## Learning in public

- [SystemVerilog DV Learning Lab](https://github.com/ashishkommineni/systemverilog-dv-learning-lab) — nine example-first sections covering language fundamentals, arrays, OOP, constraints, concurrency, interfaces, assertions, coverage, and a complete non-UVM mini environment.
- [UVM Verification Learning Series](https://github.com/ashishkommineni/uvm-verification-learning-series) — twenty-two lessons built around one executable mini-bus environment, including factory, configuration, TLM, callbacks, virtual sequences, RAL, phasing, reset, debug, and interview preparation.
- [VLSI Interview Preparation](https://github.com/ashishkommineni/vlsi-interview-preparation) — a question-first revision path designed for focused 60–90 minute study sessions.

## How I approach verification

1. Convert the specification into observable behavior, assumptions, risks, and
   verification goals before writing stimulus.
2. Drive normal traffic first, then isolate reset, boundary, error,
   backpressure, and concurrency cases.
3. Reconstruct transactions from accepted pin-level activity rather than from
   driver intent.
4. Use an independent model and scoreboard for end-to-end correctness, SVA for
   continuous temporal rules, and coverage to expose untested behavior.
5. Preserve the failing seed or scenario, find the earliest divergence, fix
   the root cause, and rerun the smallest meaningful regression.

## Technical toolbox

| Area | Working knowledge |
|---|---|
| Languages | SystemVerilog, Verilog, Python, C, shell scripting |
| Verification | UVM, SVA, constrained-random stimulus, scoreboards, functional/code coverage, regression debug |
| Interfaces | AXI4-Lite, AHB-Lite, APB3, I²C, SPI, UART |
| Digital design | RTL, FSMs, FIFOs, CDC fundamentals, pipelines, setup/hold, and STA fundamentals |
| Tools | Cadence Xcelium, Synopsys VCS/Verdi, QuestaSim/ModelSim, Vivado, Verilator, Git |

## Current focus

- Running the full protocol UVM regressions in Cadence Xcelium and preserving
  the resulting coverage evidence.
- Building a low-power Radix-4 Booth MAC with a Modified Kogge-Stone adder for
  FPGA implementation and measured synthesis results.
- Extending the RISC-V sensor hub with architectural interrupt handling,
  configurable accelerator weights, formal CDC properties, and synthesis/STA evidence.
- Evolving the scratch RV32I core toward machine CSRs, interrupt entry/return,
  RVFI-style tracing, and formal instruction checks.
- Adding formal properties and CDC/RDC evidence where exhaustive or static
  checks provide stronger confidence than simulation alone.

## Background

- Freelance VLSI Verification Engineer / Consultant — remote, Nov 2025–present
- VLSI Design & Verification Intern — Sumedha IT Pvt Ltd, Hyderabad, May–Oct 2025
- M.Tech with VLSI-focused coursework — Amrita Vishwa Vidyapeetham, Coimbatore; in progress
- B.Tech, Electrical & Electronics Engineering — RVR & JC College of Engineering, Guntur, 2024; CGPA 8.02/10
- VLSI Design & Verification training — Sumedha IT

## Publication

“Design and Implementation of PI-Based TLBO MPPT Controller for Grid-Tied PV
Microgrid,” *International Journal of Management, Technology and Engineering*,
May 2024.

## Connect

[LinkedIn](https://www.linkedin.com/in/ashish-kommineni) ·
[Email](mailto:ashishkommineni7@gmail.com)

## License

This profile repository is released under the [MIT License](LICENSE).
