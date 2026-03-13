# Energy Budget Analysis

## Assumptions

All calculations use **50% conversion efficiency** — well below the 60–75% achievable with modern permanent magnet linear generators, and far below the 90%+ of large-scale rotary generators. This conservative baseline accounts for:

- Impulsive, high-force nature of the recoil stroke (not steady-state operation)
- Thermal losses in conductor coils under repeated rapid cycling
- Real-world mechanical tolerances and alignment
- Capacitor round-trip efficiency losses (assumed 90%)

## Candidate Weapon: Mark 45 Mod 4 (5"/62 cal)

| Parameter | Value | Source |
|-----------|-------|--------|
| Projectile Mass | 31.75 kg (70 lbs) | NavWeaps |
| Muzzle Velocity | 808 m/s (2,650 ft/s) | NavWeaps / Mark 42 specs |
| Muzzle Energy | ~10.36 MJ | Calculated: ½mv² |
| Rate of Fire | 16–20 rds/min | USN Fact File |
| Recoil Stroke | 20–29 inches (51–74 cm) | NavWeaps |
| Recoiling Mass (est.) | 3,000–4,000 kg | Estimated from mount weight |
| Firing Energy (ERGM config) | 18 MJ | NavWeaps Mod 4 data |

## Recoil Energy Calculation

Using momentum conservation:

**Projectile momentum:** 31.75 kg × 808 m/s = 25,654 kg·m/s

Propellant gases add additional momentum (typically 1.5–2× projectile momentum for naval guns).

**Estimated total recoil momentum:** ~40,000–50,000 kg·m/s

**Recoiling mass:** ~3,500 kg (barrel, breech, slide assembly)

**Recoil velocity:** 40,000 ÷ 3,500 = ~11.4 m/s (upper estimate) to 50,000 ÷ 3,500 = ~14.3 m/s

**Recoil kinetic energy:** ½ × 3,500 × (11.4)² = ~227 kJ (upper) to ½ × 3,500 × (8)² = ~112 kJ (lower)

**Working midpoint: ~125 kJ per recoil stroke**

## Conversion Chain

| Step | Calculation | Result |
|------|------------|--------|
| Raw recoil KE | Midpoint estimate | 125 kJ |
| × 50% generator efficiency | 125 × 0.50 | 62.5 kJ electrical |
| × 90% capacitor round-trip | 62.5 × 0.90 | **56.25 kJ usable** |

## Sustained Fire Output

| Metric | Calculation | Result |
|--------|------------|--------|
| Energy per minute (20 rds/min) | 56.25 × 20 | 1,125 kJ = 1.125 MJ |
| Equivalent continuous power | 1,125 ÷ 60 | **18.75 kW** |
| Energy in 5-min engagement | 56.25 × 100 | 5.625 MJ |
| Energy in 10-min engagement | 56.25 × 200 | **11.25 MJ** |

## What This Powers

| System | Power Requirement | REHD Can Supply |
|--------|------------------|-----------------|
| HELIOS laser (1 sec burst) | 60 kJ | Yes — 1 shot per gun round |
| ODIN dazzler (continuous) | ~10–20 kW (est.) | Yes — continuous operation during gun fire |
| HELIOS continuous operation | 60 kW | Partial — ~31% of requirement from single gun |
| Supplemental grid power | Variable | 18.75 kW continuous offset |

## Scaling

| Weapon System | Est. Recoil KE/Shot | Usable @50% | Power @ Max ROF |
|--------------|-------------------|-------------|-----------------|
| Mk 45 (5"/62) | ~125 kJ | ~56 kJ | ~18.75 kW |
| 155mm AGS (Zumwalt) | ~300–500 kJ | ~135–225 kJ | ~27–45 kW |
| Hypothetical 8" | ~500 kJ–1 MJ | ~225–450 kJ | ~45–90 kW |
