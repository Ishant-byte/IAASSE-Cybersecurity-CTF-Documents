# Memory Forensics

- **Platform:** TryHackMe
- **Domain:** Digital forensics
- **Difficulty:** Easy

## Objective
Analyze a memory dump to identify processes, system artefacts, and potential evidence of suspicious activity using Volatility.

## Methodology
1. Identified the memory-image format and determined the operating-system context supported by the image.
2. Used appropriate Volatility plugins to enumerate process information, including process-list and process-tree views; compared results to look for inconsistencies.
3. Reviewed relevant artefacts such as network connections, command-line information, and suspicious process relationships where supported by the image and plugin version.
4. Correlated observations and recorded the evidence needed to support any conclusion.

## Tools
Volatility, the supplied memory image, and supporting analysis utilities as needed.

## Findings
The intended outcome of this workflow was to learn about how memory forensics is done in real world. It was also found that real world memory forensics is much more complex than expected. 

## Lessons learned
Memory analysis is sensitive to operating-system context, plugin/version differences, and the completeness of the image. Cross-check results across multiple views instead of treating one plugin's output as definitive.
