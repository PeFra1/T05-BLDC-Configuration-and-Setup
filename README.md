# T05 - BLDC Configuration and Setup

## Overview

Task T05 focuses on **BLDC motor configuration for Trend and Differential motors** in **trapezoid BLDC mode**. The goal is to configure VESC parameters for maximum responsiveness and smooth operation.

### Key Objectives

1. **Trapezoid BLDC Mode Configuration**
   - Configure VESC for trapezoidal commutation (not sinusoidal)
   - Optimize motor parameters for best performance

2. **Motor Parameter Tuning**
   - Pole pairs (most critical for BLDC)
   - Resistance (R) - affects current control
   - Inductance (L) - affects current ramp
   - Flux linkage (λ) - affects back-EMF estimation

3. **Performance Goals**
   - Maximum responsiveness (fast current control)
   - Smooth operation (no cogging, minimal torque ripple)
   - Stable at low and high speeds

### Motor Types

- **Trend Motor**: T-Motor MN505-S KV320 (50A, 1200W, 6S LiPo)
- **Differential Motor**: T-Motor MN501-S KV300 (50A, 1200W, 6S LiPo)

### Hardware

| Item | Description |
|------|-------------|
| VESC Duet XS60 | Dual motor VESC (Trend + Diff) - USB shows 2 separate VESC addresses |
| Trend Motor | T-Motor MN505-S KV320 (BLDC, 50A, 1200W) |
| Diff Motor | T-Motor MN501-S KV300 (BLDC, 50A, 1200W) |
| Power Supply | Personal 12V / 1A lab power supply |

### CAN Bus

**Not used** - VESC Duet XS60 with USB connection shows 2 separate VESC addresses to PC, eliminating need for CAN bus in this setup.

## Files

| File | Description |
|------|-------------|
| README.md | This file |
| Task.md | Detailed task description |
| STATUS.md | Current status |
| WORKLOG.md | Development log |
| timesheet.md | Time tracking |
| specification/ | Technical specifications |
| configs/ | VESC configuration files |
| scripts/ | LBM/Lisp scripts |
| docs/ | Hardware docuemntation  |


## Notes

- **Pole pairs** is the most critical parameter - incorrect value will cause poor performance or no rotation
- BLDC trapezoidal mode requires accurate back-EMF estimation
- Startup parameters affect smoothness - too high duty = jerky start, too low = no start
- Builds on T01-T04 infrastructure
- Uses same VESC Tool version (7.00)