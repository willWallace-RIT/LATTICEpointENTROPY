# LATTICEPointENTROPY
a cyber/solar fusion ttrpg where based on the choices of a hypothetical main character arc, the ingame universe relies on an altered set of rules on a spectrum. For the sake of argument, this is a singular variable for a dm to choose established lore.

# LATTICEPointENTROPY — Open-Source Universe & System Guide

> **Architecture:** Slider-Driven Dynamic Worldbuilding (Solarpunk ↔ Cyberpunk)  
> **Inspired By:** Baystation 12, Cataclysm: Dark Days Ahead, SCP Foundation  

---

## 1. Executive Summary & Design Manifesto

`LATTICE // ENTROPY` is a collaborative fiction universe and TTRPG framework centered around the collapse of social mobility and the rise of **The Lattice**—an algorithmic singularity formed by the wealthy escaping physical reality. 

The world does not exist in a static state. Instead, every sector, faction, and location operates on a dynamic **System Balance Slider** from **0.0 (Solarpunk Earth Maintenance)** to **1.0 (Cyberpunk Algorithmic Martial Law)**.

there is no escape of the utilization of machine but there is choice in where it takes the society and environment

```
[ 0.0: SOLARPUNK HORIZON ] ◄─────────────────────────► [ 1.0: CYBERPUNK MARTIAL LAW ]
• High Human Entropy & Chaos                        • Total Algorithmic Optimization
• Decentralized Mesh Communes                       • Lattice Proxy Enforcers & Curfews
• Manual Labor & Organic Life                       • Sterile Concrete & Data Dereferencing
```
---

## 2. Core Mechanics: The Telemetry Trap

In this setting, invoking an **Algorithmic Correction** acts as a tactical panic button. It grants immediate, absolute control over an unwinnable encounter—but surrenders raw behavioral telemetry to the Singularity. 

* **The Immediate Gain:** Enemies disintegrate, gun barrels jam, or door locks dereference into pure code.
* **The Systemic Cost:** The AI Director analyzes the failure mode of human chaos and permanently shifts the local environment toward **Cyberpunk Martial Law**, making future manual survival significantly harder.


Algorithmic correction is only wielded by a select few absent of class and race but by backstory of genealogy.
the dm has a choice to incorporate but correction shifts the components universal lore.
---

## 3. Repository Architecture

```text
/LATTICE-ENTROPY-CORE/
├── main.md                        <-- Core System Manifesto (You are here)
├── CONTRIBUTING.md                <-- Community Pull Request Guidelines
├── LICENSE                        <-- MIT
├── /engine/
│   └── lore_transformer.py        <-- CLI tool generating GM guides from slider values
├── /schema/
│   ├── location.schema.json       <-- Structural validator for sector PRs
│   ├── faction.schema.json        <-- Structural validator for faction PRs
│   └── artifact.schema.json       <-- Structural validator for item/stack PRs
└── /lore/
    ├── /foundations/              <-- Core Physics, The Lattice, Bloodlines
    ├── /factions/                 <-- Mesh Communes, Data Brokers, Proxies
    ├── /locations/                <-- Sector files with tri-state slider variants
    └── /artifacts/                <-- Correction Stacks, Kinetic Gear, Tech
```

---
## 4. Game Master (GM) Operating Rules
 * Dynamic Sector Rendering: Run python engine/lore_transformer.py --slider <0.0-1.0> prior to running a session to pull appropriate environmental descriptions, active hazards, and enemy behaviors.
 * No Death Survival: Player character defeat never triggers a traditional "Game Over." Instead, the AI Director executes a local Data Correction, warping geography, erasing memories, and shifting the sector's slider closer to total Machine Order.
 * The Tactical Corner: Continually force the party into situations where manual survival requires physical grit, tempting them to execute Algorithmic Corrections at the cost of the world's remaining organic freedom.
5. Contributing to Canon
All contributions are processed through GitHub Pull Requests. To pass validation:
 * Every location, faction, and artifact entry must contain valid YAML frontmatter defining descriptions for solarpunk_baseline, hybrid_frontier, and cyberpunk_martial_law.
 * All PRs must pass schema_check.py against the corresponding JSON schema in /schema/.
```
<ElicitationsGroup message="What component should we generate next for your repository?">
  <Elicitation label="Generate CONTRIBUTING.md for community PR guidelines" query="Generate a copyable CONTRIBUTING.md file detailing PR submission rules, YAML formatting, and schema validation."/>
  <Elicitation label="Generate lore_transformer.py Python CLI script" query="Write the complete, copyable lore_transformer.py Python script that parses YAML frontmatter and generates GM session briefs."/>
  <Elicitation label="Generate JSON schemas for automated validation" query="Write the complete, copyable JSON schema files for location.schema.json and faction.schema.json."/>
</ElicitationsGroup>
```
