# SMP Server — Minecraft Multiplayer Project

A Minecraft multiplayer server focused on competitive/cooperative survival, 
virtual economy, and a fully custom character progression system. A format 
known as SMP, but built with systems that don't exist in vanilla Minecraft.

---

## What makes it different?

The server has a difficulty progression tied to exploration. The further a player 
moves from the central spawn point, the stronger the mobs become: more HP, more 
damage, more resistance. Exploration is genuinely dangerous.

**Does the difficulty only punish, or does it also reward?**  
Stronger mobs drop more XP. That XP feeds a vertical progression system split 
into skill trees: combat, resistance, agility, farming, and others. Leveling up 
grants character stats and unlocks active and passive abilities. A dedicated 
player is visibly stronger than a casual one.

**Doesn't that create a hostile environment for new players?**  
Yes and no. The gap exists by design, but it was carefully calibrated to avoid 
being unfair. A prepared new player can beat a veteran. The advantage is 
noticeable, not insurmountable.

---

## Tech Stack

70+ plugins working together. The four pillars of the core experience:

- **AuraSkills:** manages vertical player progression and skill trees
- **LevelledMobs:** scales mob difficulty based on distance from spawn
- **AuraMobs:** bridge between LevelledMobs and AuraSkills for granular XP control
- **Skript:** internal scripting language used to build all active and passive 
  abilities

**Why use two plugins to manage mob levels?**  
LevelledMobs has superior integrations with drop and entity plugins. AuraMobs 
communicates directly with AuraSkills. Neither one alone covers the full 
requirement. Using both with clearly defined responsibilities eliminated the 
need for Skript workarounds.

---

## Problems Solved

**The gap between veterans and new players was too large.**  
Solution: reduce overall stat efficiency from 100% to 2%. Small number, correct 
result. Progression exists, but stays reasonable.

**That reduction created a new problem: progression felt imperceptible.**  
With 2% spread across multiple skill lines, a player needed to level up 4 
categories just to gain +1 base damage. Solution: limit each skill line to a 
maximum of 2 stats. Total efficiency stays at 2%, but the gain per level became 
tangible.

---

## Infrastructure and Operations

- Hosting provider selection and comparison by cost-effectiveness
- Resource allocation decisions: RAM vs CPU based on real plugin demand
- Player support: connection issues, version compatibility, gameplay problems
- Used AI tools to accelerate technical research across documentation, forums 
  and wikis, cutting hours of searching down to minutes

---

## Monetization

Virtual storefront with a model that doesn't penalize F2P players. Paid content 
delivers convenience and cosmetics, with no direct combat advantage.

Two internal currencies: **Coins** (general economy) and **Cash** (premium 
content). Cash can be obtained with real money, traded between players, or 
earned through in-game events, ensuring access to premium content without 
requiring payment.

---

## Numbers

- **900+ unique players** in 4 months of operation
- Revenue enough to sustain all infrastructure costs for **1+ year**

---

**IP:** `GoCraft.srvmc.com | 1.21.11`
