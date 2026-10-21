# T05 - BLDC Configuration and Setup

## Work Log

### 2026-10-20

| Time | Activity |
|------|----------|
| 4h | Meeting: Task T05 assignment - BLDC Configuration and Setup |

**Notes:**
- Task assigned by Ivan and Vilko
- Focus: **Trend and Differential motors in trapezoid BLDC mode**
- Goal: Maximum responsiveness + smooth operation

**Hardware received:**
- VESC Duet XS60 (dual motor, USB shows 2 separate addresses)
- Trend Motor: T-Motor MN505-S KV320 (50A, 1200W, 6S LiPo)
- Diff Motor: T-Motor MN501-S KV300 (50A, 1200W, 6S LiPo)

**CAN Bus:**
- **Not used** - VESC Duet XS60 USB connection shows 2 separate addresses to PC

**Power Supply:**
- Personal 12V / 1A lab power supply for lab testing

**Planned:**
- Identify motor specifications (KV, poles, R, L, λ)
- Configure VESC for trapezoid BLDC mode
- Tune motor parameters
- Test smooth operation

**Completed:**
- Task assignment documentation
- Hardware identification

---

### 2026-10-21

| Time | Activity |
|------|----------|
| 3h | Documentation: VESC Duet XS60 and motor documentation (MN505-S KV320, MN501-S KV300) |

**Notes:**
- Created VESC Duet XS60 documentation folder with specification.md and links.md
- Added MN505-S KV320 documentation (specifications.md, links.md, testData.md)
- Added MN501-S KV300 documentation (specifications.md, links.md, testData.md)
- Fixed hardware model name across all T05 documentation files (X560 → XS60)
- Nett time spent: 3h