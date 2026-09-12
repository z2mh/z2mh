# Engineering project notes

## MU0 processor and digital logic

COMP12111 computer-engineering coursework moving from display-decoder logic and a traffic-light finite-state machine to an MU0 processor in Verilog. My recorded commits implement and modify the MU0 ALU, datapath, registers, multiplexers and testbenches. The repository also contains MU0 assembly exercises and FPGA synthesis outputs.

The datapath connects a 12-bit program counter with 16-bit instruction and accumulator registers, operand multiplexers, an ALU, condition flags and memory address/control signals. The recovered source and commit history are preserved in the private `digital-logic-labs` repository. The source was inspected during migration; the original ModelSim/Vivado workflow was not rerun.

## Stump processor architecture

COMP22111 computer-architecture coursework centred on the 16-bit Stump processor. My recorded commits implement or modify the gate-level ALU, condition flags, control decoder, testbench and assembly exercises. The control work covers fetch, execute and memory states, register selection, instruction decoding, branch conditions and memory read/write signals.

The private `processor-design-verilog` repository also retains a course-supplied MU0 reference design used to study processor structure. That reference is clearly separated from my Stump implementation work. The source and FPGA build outputs were inspected during migration; no fresh simulator pass is claimed.

## Microcontrollers

COMP22712 coursework covering memory-mapped peripherals, processor bus reads and writes, GPIO direction, LED/LCD and switch interfaces, interrupts and SystemVerilog peripheral testbenches.

The accessible GitLab repository currently contains one staff-authored initial commit with the supplied `User_Peripheral.sv` template and testbench. No student-authored submission or additional branch was available, so I represent the module here without presenting the starter template as my completed implementation.

## RISC-V assembly

Four COMP15111 lab repositories cover instruction execution, registers, control flow, memory addressing, strings, ABI conventions, methods and stack operations using the Bennett RISC-V simulator. The submitted solutions and written answers retain their original coursework context and attribution.

## Solar-system visualization

A Three.js scene showing a solar system through perspective and orthographic cameras side by side. The implementation includes a comet with custom Blinn–Phong shaders, an instanced belt of 1,500 asteroids, mouse camera controls and an automatic camera mode.

The scene was checked in a browser: both views rendered and the animation control worked. The preview is an actual screenshot of the project. Planet textures are credited to [Solar System Scope](https://www.solarsystemscope.com/textures/) under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

## EventLite

A team application from COMP23412, Group G15, for managing events and venues using Spring Boot, JPA, H2, server-rendered pages and REST endpoints. My recorded contributions include event maps, a Mastodon timeline, API links and validation fixes. The project builds on university starter code and contributions from the whole team.

During migration, embedded credentials were replaced by environment configuration. The existing suite passed **117 tests**; live external services were not tested with credentials.

## Processor emulator

A COMP26020 exercise refactoring course-provided code for an 8-bit processor with a 256-byte address space. The project explores instruction classes, processor state, breakpoints, standard-library types and memory ownership.

The structural suite passed **16 test cases** and the functional suite passed **67 test cases** after a null-pointer compatibility update to the supplied tests. No sanitizer result is claimed.

## Cache simulator

A Python memory-cache simulator with an uncached baseline and cyclic, LRU, MRU and LFU eviction policies. A companion set of access traces explores how policy choices affect cache behaviour.

The supplied unittest suite passed **30 tests**. The implementation and harness retain the original coursework context and attribution.

## Matrix library

A C library implementing matrix allocation, cleanup, arithmetic, transposition and file operations. The local header, sample inputs and Unity test harness were recovered alongside the submitted implementation.

The supplied test suite passed **17 tests**.

## Register allocation

A Python command-line program that colours an interference graph by ranking vertices by degree and assigning available colours. It demonstrates deterministic greedy allocation with up to 26 register colours. This strategy does not guarantee an optimal colouring.

A three-vertex example produced valid distinct colours. This was a smoke check rather than exhaustive verification.

## Additional study areas

Other repositories document Haskell quadtrees, Solidity state machines, PHP/MySQL employee management, JavaFX and Java practice, and probability/data notebooks. Some are unfinished learning exercises and are labelled accordingly.

**Source access:** Academic repositories are currently private. Team projects and starter code retain their original attribution. Verification counts describe checks run on 12 September 2026, not claims about production readiness.
