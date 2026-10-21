# T05 - Hardware Setup

## Equipment List

| Item | Description | Quantity | Notes |
|------|-------------|----------|-------|
| VESC Duet XS60 | Dual motor VESC (Trend + Diff) | 1x | High-power VESC for BLDC, USB shows 2 separate addresses |
| Trend Motor | T-Motor MN505-S KV320 | 1x | BLDC motor (50A, 1200W, 6S) |
| Diff Motor | T-Motor MN501-S KV300 | 1x | BLDC motor (50A, 1200W, 6S) |
| Power Supply | Personal 12V / 1A lab power supply | 1x | Personal supply for lab testing |

## Motor Specifications

### Trend Motor (T-Motor MN505-S KV320)
- **Model:** MN505-S Fixed Wing Motor
- **KV:** 320 RPM/V
- **Configuration:** TBD (24N28P? Check datasheet)
- **Max Current:** 50A (l_current_max), 75A peak
- **Max Power:** 1200W
- **Max Voltage:** 6S LiPo (22.2V)
- **CAN ID:** TBD (configure in VESC)
- **Datasheet:** [TMotor MN505-S](https://store.tmotor.com/product/mn505-s-fixed-wing-motor.html)
- **FOC Config:** R=?, λ=?, L=?

### Differential Motor (T-Motor MN501-S KV300)
- **Model:** MN501-S Fixed Wing Motor
- **KV:** 300 RPM/V
- **Configuration:** TBD (24N28P? Check datasheet)
- **Max Current:** 50A (l_current_max), 75A peak
- **Max Power:** 1200W
- **Max Voltage:** 6S LiPo (22.2V)
- **CAN ID:** TBD (configure in VESC)
- **Datasheet:** [TMotor MN501-S](https://store.tmotor.com/product/mn501-s-fixed-wing-motor.html)
- **FOC Config:** R=?, λ=?, L=?

### CAN Bus

**Not used** - VESC Duet XS60 with USB connection shows 2 separate VESC addresses to PC, eliminating need for CAN bus in this setup.

## Power Supply Notes

**Lab Testing:**
- Personal 12V / 1A power supply (sufficient for both motors at low duty cycle)

**Flight Operation:**
- Both motors: 6S LiPo (22.2V) - Questionable!!!
- Battery management: separate BMS per battery pack