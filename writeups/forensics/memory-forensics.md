# Memory Forensics

- **Platform:** TryHackMe
- **Domain:** Digital forensics
- **Difficulty:** Easy
- **Status:** Assumed completed for this portfolio draft — verify against your actual run before publishing

## Objective
Analyze a memory dump to identify processes, system artefacts, and potential evidence of suspicious activity using Volatility.

## Methodology
1. Identified the memory-image format and determined the operating-system context supported by the image.
2. Used appropriate Volatility plugins to enumerate process information, including process-list and process-tree views; compared results to look for inconsistencies.
3. Reviewed relevant artefacts such as network connections, command-line information, and suspicious process relationships where supported by the image and plugin version.
4. Correlated observations and recorded the evidence needed to support any conclusion.

## Tools
Volatility (version to be recorded), the supplied memory image, and supporting analysis utilities as needed.

## Findings
The intended outcome of this workflow is a documented inventory of processes and artefacts relevant to the challenge questions. **Replace this sentence with the specific process names, artefacts, and conclusions you actually observed.** The source document did not contain completed findings for this room, so no specific malicious process or flag is asserted here.

## Lessons learned
Memory analysis is sensitive to operating-system context, plugin/version differences, and the completeness of the image. Cross-check results across multiple views instead of treating one plugin's output as definitive.

## Evidence to add before publishing
- Sanitized output showing the relevant process/artefact observations.
- Volatility version and the plugin(s) actually used.
- A short explanation of why each observation mattered to the room's question.

> Do not leave the verification note above in a final portfolio if you have replaced it with your actual results. Never invent artefacts to make the write-up appear complete.
