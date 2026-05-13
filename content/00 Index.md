---
type: index
vault: big-mountain-expeditions
tags: [index]
---

# Big Mountain Expeditions — Dashboard

> [!info] Vault structure
> Each trip is self-contained: route playbook + its own Logistics, Gear, Training, Weather, and Guides notes. Only [[Resources]] is shared across trips.

`vault_status:: planning`
`default_style:: unguided`
`home_airport:: DEN`

## The three objectives

| Trip | Route | Summit | Days | Section |
|---|---|---:|---:|---|
| Grand Teton | Owen-Spalding | 13,775 ft / 4,199 m | 3 | [[01 Grand Teton/index|Grand Teton]] |
| Mont Blanc | Trois Monts | 15,777 ft / 4,808 m | 5 | [[02 Mont Blanc/index|Mont Blanc]] |
| Denali | West Buttress | 20,310 ft / 6,191 m | 21 | [[03 Denali/index|Denali]] |

---

## Live dashboard

### All expeditions
```dataview
TABLE country, days_total, max_elevation_m, season, style, status
FROM "01 Grand Teton" OR "02 Mont Blanc" OR "03 Denali"
WHERE type = "expedition"
SORT max_elevation_m ASC
```

### Open logistics across all trips
```dataview
TABLE expedition, category, status, file.folder
FROM "01 Grand Teton" OR "02 Mont Blanc" OR "03 Denali"
WHERE type = "logistics" AND status = "open"
SORT expedition ASC, category ASC
```

### Gear lists
```dataview
TABLE expedition, weight_target_kg, status
FROM "01 Grand Teton" OR "02 Mont Blanc" OR "03 Denali"
WHERE type = "gear_list"
SORT expedition ASC
```

### Weather sources
```dataview
TABLE expedition, primary_forecast, season_window
FROM "01 Grand Teton" OR "02 Mont Blanc" OR "03 Denali"
WHERE type = "weather"
```

### All open todos
```dataview
TASK
FROM ""
WHERE !completed
GROUP BY file.folder
```

---

## Decisions (cross-cutting)

- **Order:** Teton → Mont Blanc → Denali. Teton is a long weekend and a sanity check on rope-team movement at moderate altitude. Mont Blanc layers in real glacier travel and a full alpine summit day at 4,800 m. Denali is the capstone — three weeks, cold-weather systems, hauling, full expedition logistics.
- **Default style:** unguided. Background: unguided Rainier, Cotopaxi summit, Chimborazo summit. Mont Blanc Trois Monts is the only one where guides are the default for most parties.
- **Partners:** all three need rope partners. Solo on Denali is permitted but a very different game.
- **Home airport:** DEN. JAC for Teton (or drive ~9h), GVA for Mont Blanc (CDG/ZRH backup), ANC for Denali (then TKA / Talkeetna).

---

## Open questions (vault-wide)

- [ ] Identify rope partners for each objective (different for each in all likelihood)
- [ ] Decide whether to chain Teton + an Exum guide day for skills refresher (crevasse rescue, short-roping) before Mont Blanc
- [ ] Confirm insurance covers technical alpine climbing + helicopter evac (default travel insurance usually does **not**)
- [ ] Budget envelope per trip — see per-trip Money pages
- [ ] Pick a year/season window for Denali (May–June) and work backwards on training timeline

---

## Quick navigation by trip

### [[01 Grand Teton/index|Grand Teton]]
- [[01 Grand Teton/01 Logistics/Travel & Flights|Travel]] · [[01 Grand Teton/01 Logistics/Accommodations|Accommodations]] · [[01 Grand Teton/01 Logistics/Permits & Registration|Permits]] · [[01 Grand Teton/01 Logistics/Insurance|Insurance]] · [[01 Grand Teton/01 Logistics/Money|Money]] · [[01 Grand Teton/01 Logistics/Health & Acclimatization|Health]]
- [[01 Grand Teton/02 Gear List|Gear]] · [[01 Grand Teton/03 Training & Skills|Training]] · [[01 Grand Teton/04 Weather & Conditions|Weather]] · [[01 Grand Teton/05 Guides & Operators|Guides]]

### [[02 Mont Blanc/index|Mont Blanc]]
- [[02 Mont Blanc/01 Logistics/Travel & Flights|Travel]] · [[02 Mont Blanc/01 Logistics/Accommodations|Accommodations]] · [[02 Mont Blanc/01 Logistics/Permits & Registration|Permits]] · [[02 Mont Blanc/01 Logistics/Insurance|Insurance]] · [[02 Mont Blanc/01 Logistics/Money|Money]] · [[02 Mont Blanc/01 Logistics/Health & Acclimatization|Health]]
- [[02 Mont Blanc/02 Gear List|Gear]] · [[02 Mont Blanc/03 Training & Skills|Training]] · [[02 Mont Blanc/04 Weather & Conditions|Weather]] · [[02 Mont Blanc/05 Guides & Operators|Guides]]

### [[03 Denali/index|Denali]]
- [[03 Denali/01 Logistics/Travel & Flights|Travel]] · [[03 Denali/01 Logistics/Accommodations|Accommodations]] · [[03 Denali/01 Logistics/Permits & Registration|Permits]] · [[03 Denali/01 Logistics/Insurance|Insurance]] · [[03 Denali/01 Logistics/Money|Money]] · [[03 Denali/01 Logistics/Health & Acclimatization|Health]]
- [[03 Denali/02 Gear List|Gear]] · [[03 Denali/03 Training & Skills|Training]] · [[03 Denali/04 Weather & Conditions|Weather]] · [[03 Denali/05 Guides & Operators|Guides]]

### Shared reference
- [[Resources]] — books, websites, podcasts, gear shops

---

## Parked (future / out-of-scope)

- **Aconcagua** — would slot between Mont Blanc and Denali for altitude experience, parked unless schedule allows
- **Cassin Ridge (Denali)** — only after West Buttress, never as a first Denali trip
- **Cosmiques Arête / Tacul Triangle** — Chamonix warm-ups, would chain naturally with Mont Blanc trip
- **Eiger Mittellegi, Matterhorn Hörnli** — adjacent classics if a longer Alps trip materializes
