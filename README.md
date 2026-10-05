# Ashish Kommineni

### Design Verification Engineer | RTL Design · SystemVerilog · UVM · SVA

Hello, I’m Ashish. I am pursuing an M.Tech with a VLSI focus at Amrita Vishwa Vidyapeetham, Coimbatore. My main interest is design verification: understanding a specification, identifying what can go wrong, and building checks that detect those failures without depending on manual waveform inspection.

Most of my projects begin with a small behavioral contract. I implement the RTL, write directed tests for the risky corners, add constrained-random stimulus, and compare observed DUT behavior against an independent model. This profile is my engineering notebook, so executed results, expected results, and tool limitations are kept separate.

## Selected engineering work

| Project | What I designed | What I verified | Evidence |
|---|---|---|---|
| [7 Days of RTL](https://github.com/ashishkommineni/7-days-of-rtl) | Seven blocks covering arbitration, partial writes, flow control, CDC, pipelining, and packet routing | Self-checking reference models, SVA, conservation checks, and one-command regression | [Seven-project regression record](https://github.com/ashishkommineni/7-days-of-rtl/blob/main/docs/verification_report.md) |
| [AXI4-Lite Memory Slave](https://github.com/ashishkommineni/axi4-lite-uvm-verification) | Independent AW/W acceptance, byte strobes, decode responses, and read/write backpressure | UVM agent, monitor-reconstructed transfers, byte-aware scoreboard, channel-skew coverage, and stable-VALID assertions | [Executed checks and simulator boundary](https://github.com/ashishkommineni/axi4-lite-uvm-verification/blob/main/docs/verification_results.md) |
| [Asynchronous FIFO](https://github.com/ashishkommineni/asynchronous-fifo-uvm-verification) | Gray-coded pointers, two-flop synchronizers, and independent read/write clocks | Dual UVM agents, cross-domain ordering scoreboard, boundary assertions, and unrelated-clock smoke tests | [Executed checks and CDC limitations](https://github.com/ashishkommineni/asynchronous-fifo-uvm-verification/blob/main/docs/verification_results.md) |

These are the three projects I would start with in a technical discussion. They show different parts of the job: RTL design, protocol behavior, clock-domain crossing, reusable verification structure, and debug evidence.

## Protocol and IP verification

| Repository | Main engineering focus |
|---|---|
| [AHB-Lite Memory Slave](https://github.com/ashishkommineni/ahb-lite-uvm-verification) | Pipelined address/data phases, wait states, and two-cycle ERROR response |
| [APB3 Register Slave](https://github.com/ashishkommineni/apb3-uvm-verification) | Setup/access timing, programmable waits, register prediction, and `PSLVERR` |
| [I²C Write Master](https://github.com/ashishkommineni/i2c-master-uvm-verification) | Open-drain signaling, ACK/NACK behavior, pin-level decode, and clock-stretch awareness |
| [SPI Master](https://github.com/ashishkommineni/spi-master-uvm-verification) | Modes 0–3, edge selection, chip-select behavior, and full-duplex loopback |
| [UART](https://github.com/ashishkommineni/uart-uvm-verification) | Configurable word length, parity, framing, and serial end-to-end checking |
| [Synchronous FIFO](https://github.com/ashishkommineni/synchronous-fifo-uvm-verification) | Occupancy boundaries, simultaneous read/write, ordering, overflow, and underflow |

Each repository contains synthesizable RTL, UVM source, SVA, functional coverage, a self-checking portable smoke test, a verification plan, and exact run commands. The result documents state what was actually executed; Xcelium commands are not presented as proof unless a corresponding run record exists.

## Learning in public

- [SystemVerilog DV Learning Lab](https://github.com/ashishkommineni/systemverilog-dv-learning-lab) — nine example-first chapters covering language fundamentals, arrays, OOP, constraints, concurrency, interfaces, assertions, coverage, and a complete non-UVM mini environment.
- [UVM Verification Learning Series](https://github.com/ashishkommineni/uvm-verification-learning-series) — twenty-two lessons built around one executable mini-bus environment, with focused examples for factory, configuration, TLM, callbacks, virtual sequences, RAL, phasing, reset, and 80 interview questions.

I use these repositories to practise explaining not only the syntax, but also object ownership, transaction flow, sampling, race avoidance, scoreboard independence, and end-of-test correctness.

## How I approach verification

1. Write the expected behavior and assumptions before writing stimulus.
2. Drive legal traffic first, then isolate boundary, error, reset, and backpressure cases.
3. Reconstruct transactions in the monitor from accepted pin-level activity rather than driver intent.
4. Use a reference model and scoreboard for data correctness, SVA for continuous protocol rules, and coverage for missed scenarios.
5. Preserve the failure, explain the root cause, and rerun the smallest useful regression before claiming a fix.

## Technical toolbox

| Area | Working knowledge |
|---|---|
| Languages | SystemVerilog, Verilog, Python, C, shell scripting |
| Verification | UVM, SVA, constrained-random stimulus, scoreboards, functional/code coverage, regression debug |
| Interfaces | AXI4-Lite, AHB-Lite, APB3, I²C, SPI, UART |
| Digital design | RTL, FSMs, FIFOs, CDC fundamentals, pipelines, setup/hold and STA fundamentals |
| Tools | Cadence Xcelium, Synopsys VCS/Verdi, QuestaSim/ModelSim, Vivado, Verilator, Git |

## Current focus

- Closing functional and assertion coverage on the protocol projects with Cadence Xcelium.
- Building a low-power Radix-4 Booth MAC with a Modified Kogge-Stone adder for FPGA implementation.
- Developing one integrated RTL/UVM capstone that combines control registers, data movement, interrupts, and CDC instead of treating every block in isolation.

## Experience and education

- Freelance VLSI Verification Engineer / Consultant — remote, Nov 2025–present
- VLSI Design & Verification Intern — Sumedha IT Pvt Ltd, Hyderabad, May–Oct 2025
- M.Tech with VLSI-focused coursework — Amrita Vishwa Vidyapeetham, Coimbatore; in progress
- B.Tech, Electrical & Electronics Engineering — RVR & JC College of Engineering, Guntur, 2024; CGPA 8.02/10
- VLSI Design & Verification training — Sumedha IT

## Publication

“Design and Implementation of PI-Based TLBO MPPT Controller for Grid-Tied PV Microgrid,” *International Journal of Management, Technology and Engineering*, May 2024.

## Connect

[LinkedIn](https://www.linkedin.com/in/ashish-kommineni) · [Email](mailto:ashishkommineni7@gmail.com)

## License

This profile repository is released under the [MIT License](LICENSE).
