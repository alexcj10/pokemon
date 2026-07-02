# Dataset Overview

This dataset contains information about Pokémon, including their battle statistics, physical characteristics, abilities, evolution details, type effectiveness, and regional forms.

---

# Dataset Column Descriptions

| Column | Description |
|--------|-------------|
| **Number** | Unique Pokédex number assigned to each Pokémon. Some Pokémon appear multiple times due to alternate forms. |
| **Name** | Name of the Pokémon. |
| **Type 1** | Primary Pokémon type. |
| **Type 2** | Secondary Pokémon type (if available). |
| **Abilities** | Special abilities possessed by the Pokémon. |
| **HP** | Hit Points (Health). Determines how much damage a Pokémon can take. |
| **Att** | Physical Attack stat. |
| **Def** | Physical Defense stat. |
| **Spa** | Special Attack stat. |
| **Spd** | Special Defense stat. |
| **Spe** | Speed stat. Determines which Pokémon attacks first in battle. |
| **BST** | Base Stat Total. Sum of HP, Attack, Defense, Special Attack, Special Defense, and Speed. |
| **Mean** | Average of the six battle stats. |
| **Standard Deviation** | Measures how balanced or uneven the six battle stats are. |
| **Generation** | Generation in which the Pokémon was introduced. |
| **Experience Type** | Growth rate used for leveling up. |
| **Experience to Level 100** | Total experience required to reach Level 100. |
| **Final Evolution** | Indicates whether the Pokémon is in its final evolutionary stage. |
| **Catch Rate** | Indicates how easy or difficult the Pokémon is to catch. Higher values indicate easier capture. |
| **Legendary** | Indicates whether the Pokémon is Legendary. |
| **Mega Evolution** | Indicates whether the Pokémon has a Mega Evolution form. |
| **Alolan Form** | Indicates whether the Pokémon has an Alolan regional form. |
| **Galarian Form** | Indicates whether the Pokémon has a Galarian regional form. |
| **Against Normal – Against Fairy** | Damage multiplier received when attacked by each Pokémon type. |
| **Height** | Height of the Pokémon (meters). |
| **Weight** | Weight of the Pokémon (kilograms). |
| **BMI** | Body Mass Index calculated from height and weight. |

---

# Type Effectiveness

The **Against** columns represent the damage multiplier a Pokémon receives when attacked by a specific Pokémon type.

| Value | Interpretation |
|------:|----------------|
| **0** | Immune (No damage received) |
| **0.25** | Highly resistant (¼ damage) |
| **0.5** | Resistant (½ damage) |
| **1** | Normal damage |
| **2** | Weak (2× damage) |
| **4** | Highly weak (4× damage) |

Examples:

- **Against Fire = 2** → Fire-type attacks deal twice the normal damage.
- **Against Water = 0.5** → Water-type attacks deal half the normal damage.
- **Against Ground = 0** → Ground-type attacks have no effect.

---

# Evolution and Special Forms

### Final Evolution
Indicates whether the Pokémon is in its final evolutionary stage.
- 1 = Yes (cannot evolve further) → Final Evolution
- 0 = No (can still evolve) → Not Final Evolution

### Catch Rate
Represents how easy or difficult a Pokémon is to catch.
- Higher value = Easier to catch
- Lower value = Harder to catch

### Legendary
Indicates whether the Pokémon is Legendary.
- 1 = Legendary
- 0 = Not Legendary

### Mega Evolution
Indicates whether the Pokémon has a Mega Evolution form.
- 1 = Has Mega Evolution
- 0 = Does not have Mega Evolution

### Alolan Form
Indicates whether the Pokémon has an Alolan regional form.
- 1 = Has Alolan Form
- 0 = Does not have Alolan Form

### Galarian Form
Indicates whether the Pokémon has a Galarian regional form.
- 1 = Has Galarian Form
- 0 = Does not have Galarian Form

---

# Statistical Metrics

## Base Stat Total (BST)

BST is the sum of a Pokémon's six battle stats.

Higher BST generally indicates a stronger overall Pokémon.

---

## Mean

The average of the six battle stats.

It represents the average strength of an individual stat.

---

## Standard Deviation

Standard Deviation measures how balanced a Pokémon's six battle stats are.

- Low Standard Deviation → More balanced stats.
- High Standard Deviation → More specialized or uneven stats.

General guideline:

- **0–10** → Very balanced
- **10–20** → Moderately balanced
- **Above 20** → Highly specialized

> These are general guidelines and may vary depending on the dataset.

---

## Z-Score

The Z-Score compares a Pokémon's BST with the average BST of all Pokémon in the dataset.

Interpretation:

- **Z-Score < 0** → Below the dataset average.
- **Z-Score = 0** → Equal to the dataset average.
- **Z-Score > 0** → Above the dataset average.

In simple terms, the Z-Score indicates how far a Pokémon's overall strength is from the average Pokémon in the dataset.

---

# Important Notes

- The dataset contains alternate Pokémon forms (such as Mega, Alolan, and Galarian forms). Therefore, some Pokédex numbers appear multiple times.
- Each alternate form has different battle statistics and is treated as a separate observation.
- The **Mean** and **Standard Deviation** columns are calculated using the six battle stats of an individual Pokémon.
- The **Z-Score** is calculated using the BST values of all Pokémon in the dataset, allowing comparison across the entire population.

---

# Summary

| Metric | Description |
|---------|-------------|
| **BST** | Overall strength of a Pokémon. |
| **Mean** | Average of the six battle stats. |
| **Standard Deviation** | Indicates how balanced the six battle stats are. |
| **Z-Score** | Indicates how a Pokémon's overall strength compares with all Pokémon in the dataset. |