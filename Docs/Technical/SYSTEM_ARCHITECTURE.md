# System Architecture

## Core Components

### 1. Linear Electromagnetic Generator (LEG)

Permanent magnet linear alternator integrated into or replacing the conventional hydraulic recoil buffer. Uses the barrel's recoil stroke as the driving motion.

- **Type:** Permanent magnet synchronous linear generator
- **Stroke:** 20–29 inches (matches existing recoil stroke)
- **Peak force:** Hundreds of kN (must withstand full recoil impulse)
- **Cycle time:** ~50–100 ms per recoil event
- **Target efficiency:** 50% (conservative), 60–75% (optimistic)

### 2. Power Management Unit (PMU)

Solid-state power electronics module that receives raw AC output from the LEG, rectifies it, and routes it to the selected destination.

- Interfaces with ship's fire control system via standard data bus
- Receives mode selection commands in real-time
- Can blend power distribution across multiple modes simultaneously (e.g., 70% Mode 1, 30% Mode 4)
- Reports energy status: generation rate, storage levels, mode state

### 3. Capacitor Bank Array (CBA)

High-energy-density supercapacitor bank for rapid charge/discharge cycles.

- **Charge rate:** Full charge from single shot in <100 ms
- **Discharge rate:** Full discharge in 1–2 seconds for laser engagement
- **Cycle life:** >1 million cycles (supercapacitor advantage over batteries)
- **Modular:** Scalable to ship's power needs

### 4. Supplemental Power Bank (SPB)

Longer-duration energy storage for Mode 4 banking operations.

- Options: larger capacitor bank, lithium-ion battery, or flywheel energy storage
- Optimized for minutes-to-hours storage duration
- Grid-connected: power available to ship's electrical distribution system on demand
- Isolated from CBA: separate storage for different time-domain needs

### 5. Mechanical Energy Return System (MERS)

For Mode 2 (ROF Boost). Stores recoil energy mechanically and returns it as accelerated forward stroke.

- Options: gas spring, flywheel, electromagnetic linear motor
- Operates in mechanical domain (no electrical conversion losses)
- Can operate in parallel with LEG (partial energy to mechanical return, partial to electrical generation)

### 6. Electromagnetic Boost Coils (EBC)

⬛ *[REDACTED — Mode 3 component. See restricted version.]*

## System Integration

```
                    ┌─────────────┐
                    │  GUN FIRES  │
                    └──────┬──────┘
                           │
                    ┌──────▼──────┐
                    │   RECOIL    │
                    │   STROKE    │
                    └──────┬──────┘
                           │
              ┌────────────▼────────────┐
              │  LINEAR ELECTROMAGNETIC  │
              │      GENERATOR (LEG)     │
              └────────────┬────────────┘
                           │
              ┌────────────▼────────────┐
              │   POWER MANAGEMENT UNIT  │◄──── Fire Control System
              │         (PMU)            │      (mode selection)
              └──┬─────┬─────┬─────┬───┘
                 │     │     │     │
         ┌───▼──┐ ┌─▼───┐ ┌─▼──┐ ┌▼────┐
         │MODE 1│ │MODE 2│ │MODE│ │MODE 4│
         │ DEW  │ │ ROF  │ │ 3  │ │ BANK │
         │CHARGE│ │BOOST │ │[R] │ │      │
         └───┬──┘ └──┬──┘ └─┬──┘ └──┬───┘
             │       │      │       │
         ┌───▼──┐ ┌──▼──┐  ⬛   ┌──▼───┐
         │ CBA  │ │MERS │      │ SPB  │
         └───┬──┘ └──┬──┘      └──┬───┘
             │       │            │
         ┌───▼──┐ ┌──▼────┐  ┌───▼────┐
         │ DEW  │ │BARREL │  │ SHIP   │
         │LASER │ │RETURN │  │ GRID   │
         └──────┘ └───────┘  └────────┘
```

## Retrofit Integration

REHD is designed as a retrofit to existing gun mounts, not a new-build requirement.

**Installation approach:**
1. Remove or augment existing hydraulic recoil buffer
2. Install LEG assembly in recoil path (same dimensional envelope)
3. Mount PMU in below-deck gun equipment space
4. Install CBA and SPB in available magazine or equipment space
5. Connect PMU to fire control system data bus
6. Connect SPB to ship's power distribution panel

**Estimated installation time:** Achievable during scheduled maintenance availability (CMAV or DPIA). No drydock required. No hull cuts. No propulsion system modifications.
