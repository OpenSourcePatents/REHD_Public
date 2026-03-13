# REHD — Recoil Energy Harvesting and Directed Energy Integration

> *"Life is what happens when you're busy making plans."*
>
> This entire concept started because Netflix was down and I saw a random reel of someone shooting a gun on Facebook. I had specifically told myself to focus on anything other than defense tech today. Four hours later, this existed. Sometimes the best inventions come from the moments you weren't trying.

---

## What Is REHD?

Every time a naval gun fires, the recoil system absorbs ~125,000 joules of kinetic energy and throws it away as waste heat. **REHD captures that energy and puts it to work.**

The system replaces or augments conventional hydraulic recoil buffers with linear electromagnetic generators. When the barrel recoils, instead of wasting that energy, REHD converts it to electricity and routes it where the ship needs it most.

**The problem it solves:** The U.S. Navy cannot generate enough electrical power on its destroyers to operate directed energy weapons (lasers). Rear Admiral Ronald Boxall stated the fleet is *"out of Schlitz with regard to power."* REHD solves this using energy the ship is already producing and throwing away.

**The math (conservative, 50% efficiency):**
- **56.25 kJ** usable energy per shot from a single Mk 45 gun
- **18.75 kW** continuous equivalent power at max rate of fire
- **11.25 MJ** banked in a 10-minute engagement
- A carrier strike group with 6 REHD mounts: **112.5 kW** — nearly double a HELIOS laser system

**The cost:** Less than $2M per gun mount. That's less than one SM-2 missile — the same missile the Navy has been spending $2.4M each to shoot down $2,000 drones.

### Every shot fired charges the next fight.

---

## The Four Power Modes

| Mode | Name | Function |
|------|------|----------|
| **Mode 1** | DEW Charging | Recoil energy charges capacitor banks that feed a directed energy weapon. The gun charges the laser. |
| **Mode 2** | ROF Boost | Stored energy accelerates the barrel's return stroke, increasing rate of fire. Faster shooting → more energy → faster return → faster shooting. |
| **Mode 3** | Kinetic Energy Assist | ⬛ *[REDACTED — See restricted version]* |
| **Mode 4** | Power Banking | Energy deposited into a supplemental power bank for later use. A combat savings account. |

The fire control system selects and blends modes in real-time based on tactical conditions.

> **Note on Mode 3:** Mode 3 content has been redacted from the public release pending ITAR and Invention Secrecy Act review. The unrestricted version is available to verified U.S. DoD/military personnel upon request. See [legal/RESTRICTED_ACCESS.md](docs/legal/RESTRICTED_ACCESS.md) for details.

---

## Repository Structure

```
REHD/
├── README.md                          ← You are here
├── docs/
│   ├── modes/
│   │   ├── MODE1_DEW_CHARGING.md      ← Detailed Mode 1 description & math
│   │   ├── MODE2_ROF_BOOST.md         ← Detailed Mode 2 description & math
│   │   ├── MODE3_REDACTED.md          ← Redaction notice & access instructions
│   │   └── MODE4_POWER_BANKING.md     ← Detailed Mode 4 description & math
│   ├── technical/
│   │   ├── ENERGY_BUDGET.md           ← Full energy calculations at 50% efficiency
│   │   ├── SYSTEM_ARCHITECTURE.md     ← Component descriptions & integration
│   │   ├── FLEET_APPLICABILITY.md     ← Every ship class this works on
│   │   └── RED_SEA_SCENARIO.md        ← Minute-by-minute engagement walkthrough
│   └── legal/
│       ├── CLAIMS.md                  ← Provisional claims summary
│       ├── PRIOR_ART.md              ← Novelty statement
│       ├── RESTRICTED_ACCESS.md       ← How to request unrestricted version
│       └── COST_COMPARISON.md         ← REHD vs. alternative power solutions
├── assets/
│   └── (diagrams and drawings — TBD)
├── EXECUTIVE_BRIEF.md                 ← 60-second summary for leadership
├── ADMIRAL_BOXALL.md                  ← Open letter / message to RADM Boxall
├── REHD_Disclosure_PUBLIC.docx        ← Complete public disclosure document
└── LICENSE.md                         ← Open source, no royalty, no charge, ever
```

---

## Applicable Platforms

**Any vessel with a recoil-operated gun system.** Primary candidates:

- **Arleigh Burke DDG** (Flight I, II, IIA, III) — 1× Mk 45 — ~70 ships
- **Ticonderoga CG** — 2× Mk 45 — ~9 ships
- **Zumwalt DDG** — Advanced Gun System — 3 ships
- **Trump-class LSC** (future) — 2–3 gun mounts
- **Allied navies:** Australia, South Korea, Japan, Denmark, Spain, Greece, Thailand, Turkey

---

## Message for Admiral Boxall

See [ADMIRAL_BOXALL.md](ADMIRAL_BOXALL.md) for the full message.

**Short version:** I heard your problem. Here's an idea. No strings attached.

---

## Open Source Philosophy

This is an [Open Source Patent](https://github.com/OpenSourcePatents). No royalty. No charge. Ever.

If this concept has merit, it should be built. If the Navy wants to build it, they should build it. If Lockheed or BAE or Raytheon wants to build it, they should build it. If an allied navy wants to build it, they should build it. The idea is free. The engineering is the hard part — go do the hard part.

The only thing I ask: if you build it, and it works, let me know. I'd love to hear about it.

— Charlie
Canaan, NH
March 13, 2026

---

## Related Projects

- [FCK-U System](https://github.com/OpenSourcePatents/FCK-U-System) — Decoupled passenger cabin safety architecture (the spring energy storage concept that inspired Mode 2)
- [REVOLT](https://github.com/OpenSourcePatents/REVOLT) — 3D-printable modular wind turbine
- [THOR](https://github.com/OpenSourcePatents/THOR) — Open-source thorium reactor reference architecture
- [AIR-U](https://github.com/OpenSourcePatents/AIR-U) — 3D-printable ballistic recovery system
- [CongressWatch](https://github.com/OpenSourcePatents/Congresswatch) — Congressional anomaly scoring system
