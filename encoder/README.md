# 4-to-2 Encoder using Verilog

## Overview

This project implements a **4-to-2 Encoder** in Verilog HDL. An encoder converts one active input out of four into a 2-bit binary output.

## Inputs

- D0
- D1
- D2
- D3

## Outputs

- Y1
- Y0

## Logic Equations

Y1 = D2 + D3

Y0 = D1 + D3

## Truth Table

| D3 | D2 | D1 | D0 | Y1 | Y0 |
|----|----|----|----|----|----|
|0|0|0|1|0|0|
|0|0|1|0|0|1|
|0|1|0|0|1|0|
|1|0|0|0|1|1|

## Files

- `encoder.v` – Verilog source code
- `encoder_tb.v` – Testbench
- `encoder.vcd` – Waveform file
- `simulation_result.png` – Simulation waveform

## Simulation

### Compile

```bash
iverilog -o encoder encoder.v encoder_tb.v
```

### Run

```bash
vvp encoder
```

### Open Waveform

```bash
gtkwave encoder.vcd
```

## Applications

- Digital communication systems
- Data encoding
- Keyboard encoding
- Processor input encoding
- Interrupt handling circuits