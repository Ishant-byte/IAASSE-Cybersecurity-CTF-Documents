# c4ptur3-th3-fl4g

-Platform: TryHackMe
- Domain: Cryptography / encoding and file inspection
- Difficulty: Easy

## Objective
Solve a sequence of small puzzles involving encoding, hashing, obfuscation, and basic inspection of an image file.

## Methodology
1. Worked through the challenge prompts in order and identified the transformation likely used for each item.
2. Applied common decoding steps such as Base64 and hexadecimal decoding, checking each intermediate output.
3. Used general-purpose decoding tools such as CyberChef where they helped make transformations explicit.
4. Inspected the image file directly with basic file/string utilities when conventional decoding did not explain the result.

## Tools
CyberChef or equivalent decoders, `strings`, and basic Linux file-inspection commands.

## Findings
Several puzzles used straightforward layered decoding. 
The source notes report that a flag-like string in `meme.jpg` was discoverable through `strings`, illustrating that not every image puzzle requires a dedicated steganography tool.

## Lessons learned
Start with simple file identification and string extraction before assuming a complex hiding technique. 
Validate each transformation rather than chaining guesses blindly. In a defensive context, remember that renaming a file or embedding readable strings does not protect sensitive content.


