# Imperial Forces Forensic Analysis: Rebel Malware Investigation

This repository contains a forensic analysis report on the malware discovered on a hard drive seized from a suspected Rebel malware writer. The investigation aimed to uncover the malware’s purpose, the messages it might send, and any additional artifacts valuable to the Imperial Forces.

## Project Overview

The Imperial Forces conducted this investigation after obtaining an image of a hard drive from a suspected Rebel malware writer. The analysis focused on understanding the nature of the malware, decoding any hidden messages, and uncovering additional clues that might aid future investigations.

## Objectives

The goals of this forensic analysis were to:

1. Identify the final version of the malware and assess its function.
2. Decode any message within the final malware version.
3. Uncover other artifacts or items of intelligence that could assist the Imperial Forces.
4. Document and overcome any investigative challenges encountered.

## Methodology

The forensic investigation followed a structured approach:

1. **Data Extraction**: Analyzed files, executables, and network traces on the hard drive image.
2. **Malware Analysis**: Inspected suspicious executables and decoded potential messages within network traffic.
3. **Artifact Collection**: Located relevant items that provided insight into the Rebel’s activities.
4. **Documentation**: Compiled findings, notable artifacts, and solutions to challenges faced during the analysis.

## Key Findings

- **Malware Executables**: Two suspicious executables, `obiwan.exe` and `obiwan2.exe`, were identified. Both made network connections, with `obiwan2.exe` containing encoded messages that revealed the password `r2d2`.
- **Encrypted Message**: Using `r2d2` as a decryption key, an encrypted VeraCrypt volume was unlocked, revealing Death Star plans and messages linked to defeating Darth Vader.
- **Interesting Artifacts**: Additional files, such as "obiwan.py" and "places.sqlite," were found, likely contributing to the malware’s operation or containing relevant intelligence.

## Challenges Faced

- **Message Decoding**: Understanding the base64 encoding within `obiwan2.exe` required familiarity with decryption techniques.
- **Connecting Artifacts**: Identifying the connection between the `not-the-droids-youre-looking-for.mp3` file and the VeraCrypt volume posed an initial challenge, resolved after further analysis.

## Tools Used

- **Autopsy**: For comprehensive file analysis.
- **Wireshark**: To analyze network traffic.
- **VeraCrypt**: For decryption of the encrypted volume.
- **Base64 Decoder**: For decoding encoded messages.

## Conclusion

This analysis confirmed that the Rebel malware writer’s final version of the malware contained messages linked to strategic Rebel plans. By enhancing monitoring, encryption, and access controls, the Imperial Forces can better prevent similar security breaches.

For more details, please refer to the full investigation report in this repository.
