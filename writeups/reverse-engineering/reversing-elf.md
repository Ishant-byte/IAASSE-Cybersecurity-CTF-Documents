# Reversing ELF

- **Platform:** TryHackMe
- **Domain:** Reverse engineering
- **Difficulty:** Easy
- **Status:** Assumed completed for this portfolio draft — verify against your actual run before publishing

## Objective
Analyze ELF crackme binaries using static and dynamic techniques to understand validation logic and recover the expected challenge input or flag.

## Methodology
1. Performed initial triage with `file` and `strings` to identify the binary type and any readable clues.
2. Inspected the program's control flow and input-validation logic using a disassembler/decompiler where appropriate.
3. Used GDB to inspect execution, set breakpoints, and examine registers or memory around relevant comparisons.
4. Used `ltrace` where library-call tracing could help explain program behavior.
5. Compared the observed validation logic with runtime behavior and recorded the reasoning behind the result.

## Tools
`file`, `strings`, GDB, `ltrace`, and Ghidra or radare2 as appropriate to the actual exercise.

## Findings
The room's workflow is intended to build familiarity with combining static inspection and runtime debugging. **Replace this section with the actual binary behavior, validation logic, and results you observed.** The source document did not include completed findings, so this draft does not claim a specific recovered password or flag.

## Lessons learned
Strings alone may reveal clues but do not explain all control flow. Static analysis helps form a hypothesis, while a debugger can verify how the program behaves at runtime. Record architecture, symbols, breakpoints, and the evidence supporting each conclusion.

## Evidence to add before publishing
- A sanitized disassembly/decompiler screenshot showing the relevant validation logic.
- A debugger observation supporting your conclusion.
- Tool versions and the actual result for the challenge.

> Replace the verification note with your actual findings before submitting this as completed work. Do not invent outputs or recovered values.
