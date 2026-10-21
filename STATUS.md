# T05 - BLDC Configuration and Setup

## Status

| Task | Status |
|------|--------|
| Documentation | ✅ Updated (VESC Duet XS60, MN505-S KV320, MN501-S KV300) |
| VESC Duet XS60 docs | ✅ Created (specification.md, links.md) |
| Motor docs | ✅ Created (specifications.md, links.md, testData.md for both motors) |
| BLDC Configuration | ⏳ Planned |
| CAN Bus | ❌ Not applicable — USB shows 2 separate VESC addresses |
| System Integration | ⏳ Planned |

## Notes

- T05 focuses on **trapezoid BLDC mode** for Trend and Differential motors
- Key parameters: pole pairs, R, L, λ
- Goal: maximum responsiveness + smooth operation
- Hardware: VESC Duet XS60, MN505-S KV320 (Trend), MN501-S KV300 (Diff)
- CAN Bus not used — USB shows 2 separate VESC addresses
- Documentation completed: VESC Duet XS60, MN505-S KV320, MN501-S KV300