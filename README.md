# Victoria 3: 2000 Modern Start Project

**A modern-era overhaul mod for Victoria 3**

---

This project brings Victoria 3 into the modern world with a **year 2000 start date**, realistic borders,
demographics, and a purpose-built economic and political system covering the 21st century.

> **Status**: Active development — core systems scripted and validated; not yet fully playable.
> Country populations, buildings, and balance are being completed incrementally.

---

## Join us

- **Discord**: https://discord.gg/ANNajztEuz
- **Steam**: https://steamcommunity.com/sharedfiles/filedetails/?id=3484798458

Contributions welcome — modders, scripters, historians, artists. No experience required.

---

## Usage Policy

You may fork and modify this mod for personal or collaborative use. Do not redistribute this mod
in its original or nearly identical form without permission. Paradox Interactive retains all rights
over base Victoria 3 assets.

---

## Mod Scope

The mod replaces the vanilla 1836 start with a year-2000 bookmark, adding:

- A complete modern goods and production chain (era 6–8 techs, 20 new buildings)
- 9 new law groups covering digital, energy, healthcare, immigration, welfare, military, trade, nuclear, and media policy
- 8 modern ideologies, 9 modern interest groups with traits
- 7 modern company types
- 11 named modifiers
- 5 scripted triggers, 5 scripted effects
- 6 journal entries, 6 decisions, 21 events across 6 thematic namespaces
- Country scaffolding for 22 nations with historically accurate year-2000 law stacks

---

## Technology Tree

All modern technologies extend **eras 6, 7, and 8** on top of the vanilla tech tree.

### Era 6 — Information Age

**Production:** `internet_infrastructure`, `fiber_optics`, `mobile_telecommunications`,
`gps_navigation`, `containerized_logistics`, `precision_agriculture`, `advanced_petrochemicals`

**Society:** `globalization`, `human_rights_framework`, `microfinance`, `digital_democracy`,
`environmental_regulation`

### Era 7 — Digital Age

**Production:** `cloud_computing`, `renewable_energy`, `hydraulic_fracturing`,
`industrial_automation`, `electric_vehicles`, `biotech_engineering`, `advanced_materials`

**Society:** `social_media`, `big_data_analytics`, `international_criminal_court`,
`climate_science`, `sovereign_wealth_funds`

### Era 8 — Near Future

**Production:** `artificial_intelligence`, `quantum_computing`, `fusion_research`,
`vertical_farming`, `space_commercialization`, `carbon_capture`

**Society:** `universal_basic_income`, `digital_currency`, `ai_governance`,
`carbon_neutral_economy`, `space_law`

---

## Goods

| Good | Category | Base Cost | Chain Role |
|------|----------|-----------|------------|
| `rare_earth_elements` | industrial | 40 | Input to semiconductors, batteries |
| `lithium` | industrial | 35 | Input to batteries |
| `natural_gas` | industrial | 25 | Input to pharmaceuticals, data centers, fuels |
| `uranium` | industrial | 50 | Input to nuclear power |
| `semiconductors` | industrial | 60 | Input to electronics, guided munitions |
| `electronics` | industrial | 50 | Input to telecom, cyber, munitions, space |
| `pharmaceuticals` | industrial | 55 | Input to nuclear (safety), intelligence |
| `software` | industrial | 40 | Input to most digital and knowledge buildings |
| `batteries` | industrial | 45 | Input to telecom, renewables |
| `refined_fuel` | industrial | 30 | Input to space launch |
| `telecommunications` | industrial | 35 | Input to financial services, intelligence |
| `financial_services` | industrial | 45 | Input to software, fintech platforms |
| `digital_services` | industrial | 50 | Input to media, software, data centers |
| `media` | industrial | 30 | Terminal output; input to data centers |
| `guided_munitions` | military | 70 | Terminal output; input to space launch |
| `military_hardware` | military | 80 | Terminal output; input to space launch |
| `cyber_capability` | military | 60 | Input to intelligence operations |

---

## Buildings

| Building | Group | Unlock Tech | Notes |
|----------|-------|-------------|-------|
| `building_rare_earth_mine` | bg_modern_mining | `materials_science` | Produces rare_earth_elements + trace uranium |
| `building_lithium_mine` | bg_modern_mining | `materials_science` | Produces lithium |
| `building_natural_gas_plant` | bg_modern_extraction | — | Produces natural_gas and refined_fuel |
| `building_uranium_mine` | bg_modern_mining | `materials_science` | Produces uranium; required by has_nuclear_capability |
| `building_semiconductor_fab` | bg_modern_manufacturing | `microprocessors` | Produces semiconductors |
| `building_electronics_factory` | bg_modern_manufacturing | `consumer_electronics` | Produces electronics |
| `building_pharmaceutical_lab` | bg_modern_manufacturing | `biotech_engineering` | Produces pharmaceuticals |
| `building_software_studio` | bg_modern_manufacturing | `internet_infrastructure` | Produces software |
| `building_battery_factory` | bg_modern_manufacturing | `electric_vehicles` | Produces batteries |
| `building_telecom_network` | bg_modern_infrastructure | `mobile_telecommunications` | Produces telecommunications |
| `building_data_center` | bg_modern_manufacturing | `cloud_computing` | Produces digital_services |
| `building_financial_hub` | bg_modern_manufacturing | `digital_currency` | Produces financial_services |
| `building_media_studio` | bg_modern_manufacturing | `social_media` | Produces media |
| `building_nuclear_power_plant` | bg_modern_power | `nuclear_energy` | Consumes uranium; produces electricity |
| `building_solar_wind_farm` | bg_modern_power | `renewable_energy` | Consumes batteries+steel; produces electricity |
| `building_guided_munitions_plant` | bg_modern_military_industry | `precision_weapons` | Produces guided_munitions |
| `building_military_hardware_factory` | bg_modern_military_industry | `precision_weapons` | Produces military_hardware; required by is_great_power_2000 |
| `building_cyber_operations_center` | bg_modern_military | `artificial_intelligence` | Produces cyber_capability |
| `building_intelligence_agency` | bg_modern_government | `big_data_analytics` | Consumes cyber_capability + telecom |
| `building_space_launch_facility` | bg_modern_government | `space_commercialization` | Consumes electronics + refined_fuel + steel + guided_munitions |

> **Prompt 2.1 additions**: `building_uranium_mine` and `building_military_hardware_factory` were
> added to satisfy scripted trigger references in `has_nuclear_capability` and `is_great_power_2000`.

---

## Law Groups

| Law Group | Category | Laws |
|-----------|----------|------|
| `law_group_digital_rights` | power_structure | `law_surveillance_state`, `law_regulated_data`, `law_digital_freedom` |
| `law_group_energy_policy` | economics | `law_fossil_dependent`, `law_mixed_transition`, `law_green_mandate` |
| `law_group_healthcare_system` | distribution_of_power | `law_private_healthcare`, `law_hybrid_healthcare`, `law_universal_healthcare` |
| `law_group_immigration_policy` | distribution_of_power | `law_closed_borders`, `law_managed_migration`, `law_open_borders` |
| `law_group_welfare_state` | distribution_of_power | `law_minimal_safety_net`, `law_social_democratic_welfare`, `law_universal_basic_income` |
| `law_group_military_doctrine` | military | `law_conscription_legacy`, `law_professional_military`, `law_tech_centric_force` |
| `law_group_trade_policy` | economics | `law_protectionist`, `law_free_trade`, `law_strategic_decoupling` |
| `law_group_nuclear_policy` | military | `law_nuclear_disarmament`, `law_nuclear_deterrence`, `law_nuclear_proliferation` |
| `law_group_media_regulation` | power_structure | `law_state_controlled_media`, `law_regulated_free_press`, `law_unregulated_media` |

> Law group categories `economics` and `military` are mod-added and may require UI localization
> entries to display cleanly. Valid vanilla categories are `power_structure` and `distribution_of_power`.

---

## Ideologies

`ideology_neoliberal`, `ideology_social_democratic`, `ideology_nationalist_populist`,
`ideology_green_progressive`, `ideology_technocratic`, `ideology_religious_conservative`,
`ideology_authoritarian_statist`, `ideology_libertarian`

Each ideology defines explicit stances for all 27 modern laws.

---

## Interest Groups

| IG | Primary Ideology | Enable Condition | Trait |
|----|-----------------|-----------------|-------|
| `ig_tech_industry` | technocratic / neoliberal | `internet_infrastructure` | `ig_trait_tech_lobby` |
| `ig_military_establishment` | nationalist_populist / authoritarian_statist | always | `ig_trait_military_industrial` |
| `ig_religious_institutions` | religious_conservative | always | `ig_trait_religious_authority` |
| `ig_organized_labor` | social_democratic | always | `ig_trait_social_solidarity` |
| `ig_financial_sector` | neoliberal / libertarian | `internet_infrastructure` | `ig_trait_financial_elite` |
| `ig_green_movement` | green_progressive | `environmental_regulation` | `ig_trait_green_lobby` |
| `ig_rural_populists` | nationalist_populist | always | `ig_trait_rural_traditionalism` |
| `ig_intelligentsia` | social_democratic / green_progressive | `internet_infrastructure` | `ig_trait_academic_reformers` |
| `ig_security_services` | authoritarian_statist | `big_data_analytics` | `ig_trait_security_state` |

---

## Company Types

`company_tech_giant`, `company_energy_corp`, `company_pharma_corp`, `company_defense_contractor`,
`company_financial_conglomerate`, `company_telecom_provider`, `company_media_conglomerate`

---

## Scripted Systems

### Scripted Triggers
- `is_modern_democracy` — representative government + free/regulated press + no surveillance
- `has_nuclear_capability` — nuclear law + nuclear plant + uranium mine
- `is_tech_leader` — internet_infrastructure + cloud_computing + 3+ states with digital buildings
- `is_fossil_dependent` — fossil_dependent law + natural gas plant
- `is_great_power_2000` — recognized GP rank OR military-industrial + tech composite threshold

### Scripted Effects
- `effect_impose_sanctions` / `effect_lift_sanctions` — bilateral modifier application
- `effect_cyber_attack` — applies cyber_attack_victim modifier to target
- `effect_nuclear_test` — adds nuclear_arsenal modifier + infamy
- `effect_climate_crisis_tick` — applies climate_penalty modifier

### Modifiers
Country: `modifier_climate_penalty`, `modifier_digital_economy_bonus`, `modifier_sanctions_target`,
`modifier_sanctions_sender`, `modifier_nuclear_arsenal`, `modifier_cyber_attack_victim`,
`modifier_green_transition_subsidy`, `modifier_brain_drain`, `modifier_tech_hub`

State: `modifier_special_economic_zone`, `modifier_military_base`

### Journal Entries
`je_nuclear_ambitions`, `je_energy_transition`, `je_digital_transformation`,
`je_great_power_competition`, `je_democratic_backsliding`, `je_democratization`

### Decisions
`decision_establish_special_economic_zone`, `decision_launch_space_program`,
`decision_cyber_offensive`, `decision_impose_sanctions`, `decision_offer_development_aid`,
`decision_military_intervention`

### Events (21 total across 6 namespaces)
- **Nuclear/Strategic**: nuclear_test_detected, nuclear_crisis_response, nuclear_arms_race, nuclear_accident, disarmament_talks
- **Cyber**: cyber_attack_launched, cyber_retaliation, cyber_espionage_discovered, data_breach_scandal
- **Climate/Energy**: climate_summit, extreme_weather, oil_price_shock, renewable_breakthrough
- **Political**: populist_surge, tech_backlash, corruption_scandal, mass_protest, democratic_election_crisis
- **Economic**: financial_crisis, trade_war_escalation, tech_boom

---

## Country Scaffolding (Year 2000)

22 nations with full 9-law stacks and technology tier assignments:

| Country | Tag | Tech Tier | Notable Laws |
|---------|-----|-----------|-------------|
| United States | USA | 4 | digital_freedom, private_healthcare, nuclear_deterrence |
| China | CHI | 3 | surveillance_state, conscription_legacy, nuclear_deterrence |
| Russia | RUS | 3 | fossil_dependent, conscription_legacy, nuclear_deterrence |
| Great Britain | GBR | 4 | universal_healthcare, professional_military, nuclear_deterrence |
| France | FRA | 4 | universal_healthcare, conscription_legacy, nuclear_deterrence |
| Germany | GER | 4 | universal_healthcare, professional_military, nuclear_disarmament |
| Japan | JAP | 4 | universal_healthcare, closed_borders, nuclear_disarmament |
| India | IND | 2 | protectionist, professional_military, nuclear_deterrence |
| Brazil | BRZ | 3 | universal_healthcare, protectionist, nuclear_disarmament |
| Canada | CAN | 4 | digital_freedom, universal_healthcare, nuclear_disarmament |
| Australia | AST | 4 | digital_freedom, universal_healthcare, nuclear_disarmament |
| South Korea | ROK | 4 | digital_freedom, conscription_legacy, nuclear_disarmament |
| Mexico | MEX | 2 | fossil_dependent, minimal_safety_net, nuclear_disarmament |
| Turkey | TUR | 3 | fossil_dependent, conscription_legacy, nuclear_disarmament |
| Saudi Arabia | SAU | 3 | surveillance_state, fossil_dependent, state_controlled_media |
| Iran | IRN | 3 | surveillance_state, fossil_dependent, nuclear_deterrence |
| Israel | ISR | 4 | digital_freedom, conscription_legacy, nuclear_deterrence |
| Egypt | EGY | 2 | fossil_dependent, conscription_legacy, state_controlled_media |
| Nigeria | NGA | 2 | fossil_dependent, minimal_safety_net, nuclear_disarmament |
| South Africa | SAF | 3 | fossil_dependent, professional_military, nuclear_disarmament |
| Pakistan | PAK | 2 | protectionist, conscription_legacy, nuclear_deterrence |
| Indonesia | IDN | 2 | fossil_dependent, conscription_legacy, nuclear_disarmament |

---

## Known Limitations

1. **Law group categories**: `economics` and `military` are custom categories that may not render
   correctly without UI localization. They do not cause parse errors.

2. **`nuclear_energy` tech**: Not in the mod's tech tree. `building_nuclear_power_plant` references
   it as an unlock; this may be a valid vanilla tech or may need to be added/substituted.
   `has_nuclear_capability` deliberately avoids a tech check, using law + building state instead.

3. **`precision_weapons`, `materials_science`, `microprocessors`, `consumer_electronics`,
   `automation_robotics`**: Used in building and PM unlock conditions. Treated as vanilla V3 techs
   from earlier eras. Verify these exist in your installed game version.

4. **Military intervention**: `decision_military_intervention` is a policy commitment decision,
   not a full diplomatic play. Actual war declarations use the vanilla diplomatic system.

5. **Space goods consumption**: Space launch PMs consume `guided_munitions` and `military_hardware`
   as inputs. This is intentional (dual-use) but creates a military → space dependency.

6. **No AI starting buildings**: Country tech tier scripted effects handle technology. Physical
   building placement for 22 countries is in `common/history/buildings/` files and is still
   being completed across additional regions.

---

## Key Substitutions (Blueprint → Implementation)

| Blueprint Key | Implemented Key | File(s) |
|--------------|----------------|---------|
| `mobile_communications` | `mobile_telecommunications` | buildings, PMs |
| `internet_networking` | `internet_infrastructure` | buildings, PMs, laws |
| `signals_intelligence` | `big_data_analytics` | buildings, PMs, laws |
| `genomics` / `biotechnology` | `biotech_engineering` | buildings, PMs, laws |
| `autonomous_systems` | `artificial_intelligence` | laws |
| `nuclear_energy` (law proxy) | `advanced_petrochemicals` | laws |
| `fintech` | `digital_currency` | buildings, PMs |
| `battery_technology` | `electric_vehicles` | buildings, PMs |
| `cyber_warfare` | `artificial_intelligence` | buildings, PMs |
| `space_systems` | `space_commercialization` | buildings, PMs |
| `country_legitimacy_add` | `country_legitimacy_base_add` | IG traits |
| `building_bg_modern_power_throughput_add` | `building_power_plant_throughput_add` | laws |

---

## Validation

Two validation scripts are provided:

- `tools/validate_mod.py` — original quick reference and localization checker
- `tools/audit_release.py` — comprehensive multi-phase release audit (Prompt 2.7)

Run from the repository root:

```
python tools/validate_mod.py
python tools/audit_release.py
```

**`audit_release.py` covers:**
- Packaging check: descriptor.mod presence, events directory placement, on_actions
- Goods inventory and full production chain sanity (17 goods, 7 chains verified)
- Building / PMG / PM cross-reference integrity (20 buildings, 34 PMGs, 73 PMs)
- Technology reference resolution (mod tree + known vanilla keys)
- Law group and law completeness (9 groups, 27 laws)
- Ideology stance validity against implemented laws
- Interest group and IG trait cross-references
- Company building references
- Modifier, scripted trigger, and scripted effect resolution
- JE, decision, and event completeness (6 JEs, 6 decisions, 21 events)
- Event option mechanical-effect check with proper nested-brace handling
- Country history: law coverage per group for all 22 scaffolded nations
- Duplicate definition detection
- Localization completeness and duplicate-key detection

As of Prompt 2.7: **0 critical issues, 5 documented warnings** (see Known Limitations below).

---

## Known Limitations and Manual-Attention Items

The following items were identified during the Prompt 2.7 release audit and cannot be auto-resolved:

**1. ig_intelligentsia vanilla IG override**
The mod defines `ig_intelligentsia`, which also exists in the vanilla Victoria 3 game. This is an intentional override for the full-overhaul context (the mod replaces vanilla IGs with modern equivalents), but it may affect compatibility with other mods that assume the vanilla Intelligentsia definition.

**2. Building group parent validity**
The mod's building groups use parents such as `bg_resource`, `bg_power`, and `bg_infrastructure`. These are assumed to exist in the vanilla game but cannot be verified statically without access to Victoria 3 game files. Verify against your installed Victoria 3 version if parent group lookups fail.

**3. Modifier key patch-specific validity**
Modifier keys such as `country_minting_mult`, `building_power_plant_throughput_add`, and `state_pollution_reduction_health_mult` are used in laws and PMs. These have been cross-referenced against V3 1.4–1.6 documentation, but exact key availability may vary by patch. Verify in-game if modifiers show no effect.

**4. Dead copy of events in common/events/**
`common/events/zz_modern_events.txt` is a dead-code copy of `events/zz_modern_events.txt`. Victoria 3 loads events from `events/` only. The `common/events/` copy is not loaded and can be removed during a cleanup pass.

**5. Intentional vanilla state name overrides**
`zz_modern_states_l_english.yml` overrides vanilla names for STATE_BREST, STATE_MECKLENBURG, and STATE_MOGILEV with year-2000 names. This is intentional. The `zz_` prefix ensures the mod's names load after vanilla and win. The localization validator will report these as duplicates, which is expected and correct.

**6. Runtime verification not available**
No Victoria 3 runtime was available during this audit. Static validation covers reference integrity, syntax, localization, and packaging, but engine-specific behaviors (modifier effects, AI law weights, IG emergence, production balancing) require in-game testing.

**7. Non-scaffolded countries**
Only 22 countries have explicit law assignments for the new 9 law groups. All other vanilla countries will fall back to engine defaults for any new law group. This is a known scope gap in the country scaffolding.
