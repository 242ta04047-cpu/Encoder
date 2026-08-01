# 8-to-3 Encoder using Verilog

## Project Overview

This project implements an **8-to-3 Encoder** using Verilog HDL.

An encoder converts one active input line into its corresponding binary output.

For an 8-to-3 encoder:

- Inputs : 8
- Outputs : 3
- Active Input : One at a time

Example:

Input = 00010000

Output = 100

---

## Truth Table

| Active Input | Output |
|--------------|--------|
| D0 | 000 |
| D1 | 001 |
| D2 | 010 |
| D3 | 011 |
| D4 | 100 |
| D5 | 101 |
| D6 | 110 |
| D7 | 111 |

---

## Files

- src/encoder_8to3.v
- tb/encoder_8to3_tb.v
- simulation/waveform.png

---

## Tools Used

- Verilog HDL
- ModelSim / Vivado / Icarus Verilog
- GTKWave

---

## Simulation

Compile

iverilog -o encoder encoder_8to3.v encoder_8to3_tb.v

Run

vvp encoder

Open waveform

gtkwave encoder.vcd

---

## Expected Output

```
Input = 00000001 Output = 000
Input = 00000010 Output = 001
Input = 00000100 Output = 010
Input = 00001000 Output = 011
Input = 00010000 Output = 100
Input = 00100000 Output = 101
Input = 01000000 Output = 110
Input = 10000000 Output = 111
```