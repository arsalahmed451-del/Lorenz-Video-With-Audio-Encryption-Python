# Lorenz-Based Audio and Video Encryption and Decryption

## 1. Overview

This repository contains Python implementations and experimental evaluations of Lorenz-based chaotic encryption and decryption for digital audio and video data.

The project investigates deterministic chaotic key-stream generation, fixed-point numerical representation where implemented, reversible encryption and decryption, and statistical evaluation of the resulting outputs.

The repository contains separate audio and video implementations. Their exact processing workflows and limitations are documented in their respective directories.

## 2. Objectives

- Implement Lorenz-based chaotic key generation.
- Encrypt and decrypt supported digital media data.
- Verify correct recovery of the original input.
- Evaluate encrypted outputs using documented statistical tests.
- Compare the observed results with appropriate reference methods and published research.
- Investigate implementation requirements for a future FPGA-based system.

## 3. Repository Structure

- `audio/` — audio encryption and decryption implementation.
- `video/` — video or video-frame encryption and decryption implementation.
- `results/` — selected experimental results and statistical evaluation.
- `test_vectors/` — representative input, key-stream, encryption, and decryption examples.
- `report/` — project documentation and approved supporting material.
- `requirements.txt` — Python dependencies.

## 4. Methodology

The implementations use the Lorenz chaotic system to generate deterministic numerical sequences that are transformed into encryption key values according to each implementation's defined procedure.

The generated values are applied to the supported media data using the encryption operation implemented in the corresponding source code. Decryption applies the corresponding recovery operation.

The precise Lorenz parameters, numerical precision, key-generation rules, data representation, and processing sequence are documented alongside the relevant implementation.

## 5. Audio Implementation

The audio module supports the input formats and sample representations specified by its source code. The current WAV implementation is designed for uncompressed 16-bit PCM audio and supports mono and stereo input.

Input validation, encryption, decryption, and recovery verification should be performed using the instructions provided in `audio/`.

## 6. Video Implementation

The video module follows the frame-processing and encryption workflow implemented in `video/`. Its input requirements, supported formats, frame handling, and output generation are described in that directory.

Video processing results should be interpreted according to the actual implementation and test configuration.

## 7. Experimental Evaluation

The evaluation may include:

- Shannon entropy
- Adjacent-pixel or adjacent-sample correlation
- Histogram analysis
- Differential analysis, including NPCR and UACI where applicable
- Decryption correctness
- SHA-256 integrity verification
- Execution time and resource usage, where measured

Results must include the tested input, test configuration, and the corresponding output. Metrics are interpreted according to the media type and the limitations of each test.
