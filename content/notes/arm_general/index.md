+++
authors = ["osecur"]
title = "General ARM Notes"
description = "First post desc!"
date = 2025-03-22
updated = "2025-03-22"
[taxonomies]
tags = ["ARM", "Notes"]
+++

# ARM Versions

- ARMv1
- ARMv2
- ARMv3
- ARMv4
- ARMv5
- ARMv6
- ARMv7
- ARMv8
- ARMv9

# Data Types



# Boot Sequence

## Booting a bare-metal system

When the core has been reset, it will commence execution at the location of the reset vector in
the exception vector table (at either address 0x00000000 or 0xFFFF0000)

- In a multi-core system, enable non-primary cores to sleep

- Initialize exception vectors.

- Initialize the memory system, including the MMU.

- Initialize core mode stacks and registers.

- Initialize any critical I/O devices.

- Perform any necessary initialization of NEON or VFP.

- Enable interrupts.

- Change core mode or state.

- Handle any set-up required for the Secure world.

- Call the main() application.

