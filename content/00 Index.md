---
type: index
vault: big-mountain-expeditions
tags: [index]
---

# Big Mountain Expeditions

> [!info] Vault purpose
> Pre-trip research and planning for three target objectives, ordered by typical progression — Teton (rock + a little snow, weekend), Mont Blanc (alpine, a long weekend in Chamonix), Denali (full Alaska expedition). All planned **unguided** as the default; guide options noted per route.

`vault_status:: planning`
`default_style:: unguided`
`home_airport:: DEN`

---

## Live dashboard

### Expeditions by progression
```dataview
TABLE country, days_total, max_elevation_m, season, style, status
FROM "02 Expeditions"
WHERE type = "expedition"
SORT max_elevation_m ASC
```

### Open logistics
```dataview
TABLE category, expedition, status
FROM "01 Logistics"
WHERE status = "open"
```

### Gear lists
```dataview
TABLE expedition, weight_target_kg, status
FROM "03 Gear"
WHERE type = "gear_list"
SORT expedition ASC
```

### All open todos
```dataview
TASK
FROM ""
WHERE !completed
```

### Conditions / weather sources
```dataview
TABLE expedition, primary_forecast, season_window
FROM "05 Weather & Conditions"
WHERE type = "weather"
```

---

## Decisions (cross-cutting)

- **Order:** Teton → Mont Blanc → Denali. Teton is a long weekend and a sanity check on rope-team movement at moderate altitude. Mont Blanc layers in real glacier travel and a full alpine summit day at 4800m. Denali is the capstone — three weeks, cold-weather systems, hauling, full expedition logistics.
- **Default style:** unguided. Background: unguided Rainier, Cotopaxi summit, Chimborazo summit. Mont Blanc Trois Monts is the only one where guides are the default for most parties — see [[Mont Blanc — Trois Monts#Guided vs unguided]].
- **Partners:** all three need rope partners. Solo on Denali is permitted but a very different game.
- **Home airport:** DEN. JAC for Teton (or drive ~9h), GVA for Mont Blanc (CDG/ZRH backup), ANC for Denali (then TKA / Talkeetna).

---

## Open questions (vault-wide)

- [ ] Identify rope partners for each objective (different for each in all likelihood)
- [ ] Decide whether to chain Teton + an Exum guide day for skills refresher (crevasse rescue, short-roping) before Mont Blanc
- [ ] Confirm insurance covers technical alpine climbing + helicopter evac (default travel insurance usually does **not**)
- [ ] Budget envelope per trip — see [[Money]]
- [ ] Pick a year/season window for Denali (May–June) and work backwards on training timeline

---

## Quick navigation

### Expeditions
- [[Grand Teton — Owen-Spalding]] · [[Mont Blanc — Trois Monts]] · [[Denali — West Buttress]]

### Logistics
- [[Travel & Flights]] · [[Accommodations]] · [[Permits & Registration]] · [[Insurance]] · [[Money]] · [[Health & Acclimatization]]

### Gear
- [[Gear System Overview]] · [[Teton Gear List]] · [[Mont Blanc Gear List]] · [[Denali Gear List]]

### Training & skills
- [[Training Plan]] · [[Technical Skills]] · [[Acclimatization Strategy]]

### Weather & conditions
- [[Teton Weather & Conditions]] · [[Mont Blanc Weather & Conditions]] · [[Denali Weather & Conditions]]

### Reference
- [[Guides & Operators]] · [[Resources]]

---

## Parked (future / out-of-scope)

- **Aconcagua** — would slot between Mont Blanc and Denali for altitude experience, parked unless schedule allows
- **Cassin Ridge (Denali)** — only after West Buttress, never as a first Denali trip
- **Cosmiques Arête / Tacul Triangle** — Chamonix warm-ups, would chain naturally with Mont Blanc trip
- **Eiger Mittellegi, Matterhorn Hörnli** — adjacent classics if a longer Alps trip materializes
