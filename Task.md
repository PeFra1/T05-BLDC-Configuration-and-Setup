# T05 - BLDC Configuration and Setup

## Task

### Overview

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

4. **Motor Types**
   - **Trend Motor**: Fixed stator
   - **Differential Motor**: Nor stator or rotor are fixed. Stator is turning with a same speed (*gear ratio) of petrol engone or DICE

### Technical Requirements

#### BLDC Configuration
| Parameter | Description | Notes |
|-----------|-------------|-------|
| `si_motor_poles` | Number of pole pairs | **Critical** - must match motor datasheet |
| `si_motor_resistance` | Phase resistance (Ohms) | Affects current control tuning |
| `si_motor_inductance` | Phase inductance (Henry) | Affects current ramp rate |
| `si_motor_flux_linkage` | Flux linkage (Weber) | Affects back-EMF estimation |
| `si_foc_motor_l_l` | Line-to-line inductance | For FOC/BLDC calculations |
| `si_foc_motor_r` | Phase resistance | For voltage calculations |

#### BLDC Control Parameters
| Parameter | Description | Notes |
|-----------|-------------|-------|
| `si_bldc_duty_cycle_ramp` | Duty cycle ramp time | Smoother starts |
| `si_bldc_startup_duration` | Startup duration | Adequate for motor inertia |
| `si_bldc_startup_duty` | Startup duty cycle | Sufficient torque to start |

#### Current/Voltage Limits
| Parameter | Description | Notes |
|-----------|-------------|-------|
| `l_current_max` | Maximum current | Motor and VESC limit |
| `l_current_min` | Minimum current | Braking |
| `l_battery_cut_start` | Battery cut start | Undervoltage protection |
| `l_battery_cut_end` | Battery cut end | Hysteresis |

### Hardware

| Item | Description |
|------|-------------|
| VESC Duet XS60 | Dual motor VESC for Trend and Diff motors |
| Trend Motor | T-Motor MN505-S KV320 (BLDC, 50A max, 1200W) |
| Diff Motor | T-Motor MN501-S KV300 (BLDC, 50A max, 1200W) |
| Power Supply | Personal supply for lab setup |
| CAN Bus Wiring | None |

### Tasks

- [ ] Identify Trend and Differential motor specifications (KV, poles, R, L, λ)
- [ ] Configure VESC for **trapezoid BLDC mode**
- [ ] Input motor parameters (poles, R, L, λ)
- [ ] Configure BLDC startup parameters
- [ ] Set current and voltage limits
- [ ] Test Trend motor startup and smooth operation
- [ ] Test Diff motor startup and smooth operation
- [ ] Test coordinated control

### Notes

- **Pole pairs** is the most critical parameter - incorrect value will cause poor performance or no rotation
- BLDC trapezoidal mode requires accurate back-EMF estimation
- Startup parameters affect smoothness - too high duty = jerky start, too low = no start