# Engineering project notes

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

Other repositories document RISC-V assembly, Verilog processor and digital-logic labs, Haskell quadtrees, Solidity state machines, PHP/MySQL employee management, JavaFX and Java practice, and probability/data notebooks. Some are unfinished learning exercises and are labelled accordingly.

**Source access:** Academic repositories are currently private. Team projects and starter code retain their original attribution. Verification counts describe checks run on 12 September 2026, not claims about production readiness.
