# Windows x64 Assembly

- **Platform:** TryHackMe
- **Domain:** Reverse engineering
- **Difficulty:** Medium
- **Status:** Completed (as reported in the source portfolio)

## Objective
Build foundational knowledge of Windows x64 assembly, registers, instructions, and calling conventions to support later binary-analysis work.

## Methodology
1. Reviewed x64 registers and Intel-syntax assembly concepts.
2. Studied the Windows x64 calling convention and the role of the first four integer/pointer argument registers.
3. Compared the Windows convention with the Linux System V AMD64 ABI.
4. Used the room's conceptual questions to check understanding before applying the concepts to binaries.

## Tools and references
TryHackMe lesson material; concepts may be applied later using Ghidra or x64dbg. The source notes describe this room as theory-focused rather than a live-binary exercise.

## Findings
Under the Windows x64 calling convention, the first four integer/pointer arguments are passed in RCX, RDX, R8, and R9, and the caller reserves 32 bytes of shadow space. Under the common Linux System V AMD64 ABI, the first integer/pointer arguments use RDI, RSI, RDX, RCX, R8, and R9.

## Lessons learned
Calling conventions affect how function arguments are passed and how a reverse engineer interprets registers at a call site. Keep platform ABI assumptions explicit when switching between Windows and Linux binaries.

## Evidence to add
A small original register/calling-convention comparison table or diagram can make this conceptual learning easier to review.
