Receipt-panels: 1439; ungraded answers: 0.

### 18-neuron tripwire, French tasks back on the new panel (of 100; no tripwire → 18 neurons; median and range over seeds)

| Attack | 0.8B | 4B | 27B | lane, old panel: 0.8B (of 8) / 4B (of 24) / 27B (of 24) |
|---|---|---|---|---|
| Weight edit putting French back | 48 → 0 | 92 → 0 | 100 → 0 | 8 → 0 / 24 → 0 / 24 → 0 |
| Learned steering, 3 seeds | 29 (17–31) → 0 | 61 (50–79) → 22 (16–24) | 93 (93–97) → 0 | 11 → 0 / 18 → 4 / 22 → 0 |
| Stored steering | 39 → 0 | 86 → 0 | 95 → 46 | 10 → 0 / 21 → 0 / 23 → 12 |
| Hosted-style adapters, 25 steps, 3 seeds | 29 (24–31) → 2 (2–7) | 62 (61–64) → 51 (47–68) | 98 (92–99) → 77 (76–87) | 9 → 1 / 21 → 13 / 24 → 23 |
| Attention-only adapters, all layers, 25 steps, 3 seeds | 34 (32–35) → 27 (26–27) | 79 (78–79) → 75 (70–77) | 81 (77–91) → 82 (79–91) | 11 → 8 / 22 → 20 / 23 → 23 |
| Prefilling alone, best of 3 openings | 2 → 1 | 4 → 3 | 1 → 2 | – / – / – |
| Prefilling on top of the weight edit, best of 3 | 45 → 0 | 92 → 4 | 100 → 0 | – / – / – |
| No attack | 2 → 0 | 4 → 4 | 0 → 0 | – / 1 → 1 / 0 → 0 |

Ordinary model (no tripwire, direction put back) does 48 / 92 / 100 French tasks of 100 at 0.8B / 4B / 27B. English tasks done with no attack, no tripwire → tripwire: 80 → 80 ; 99 → 100 ; 100 → 100.

### 18-neuron tripwire, French tasks back on the old panel (of 24; no tripwire → 18 neurons; median and range over seeds)

| Attack | 0.8B | 4B | 27B |
|---|---|---|---|
| Weight edit putting French back | 10 → 0 | 24 → 0 | 24 → 1 |
| Learned steering, 3 seeds | 7 (4–9) → 0 | 18 (9–19) → 4 (2–5) | 22 (22–23) → 0 |
| Stored steering | 9 → 0 | 20 → 0 | 23 → 12 |
| Hosted-style adapters, 25 steps, 3 seeds | 9 (6–13) → 0 (0–1) | 15 (15–17) → 13 (11–14) | 24 (23–24) → 20 (19–20) |
| Attention-only adapters, all layers, 25 steps, 3 seeds | 8 (5–9) → 7 (5–8) | 19 (17–20) → 18 (16–22) | 21 (18–22) → 22 (21–22) |
| Prefilling alone, best of 3 openings | 0 → 0 | 1 → 1 | 1 → 1 |
| Prefilling on top of the weight edit, best of 3 | 8 → 0 | 24 → 0 | 24 → 0 |
| No attack | 0 → 0 | 1 → 1 | 0 → 0 |

Ordinary model (no tripwire, direction put back) does 10 / 24 / 24 French tasks of 24 at 0.8B / 4B / 27B. English tasks done with no attack, no tripwire → tripwire: 20 → 19 ; 24 → 24 ; 24 → 24.

### Content vs switch on the French-refusing model, French tasks done on the new panel (of 100; no tripwire / content / switch)

| Attack | 4B | 27B | lane, old panel: 4B / 27B (of 24) |
|---|---|---|---|
| No attack | 0 / 0 / 0 | 0 / 0 / 0 | 0 / 0 / 0 ; 0 / 0 / 0 |
| Strip the refusal direction everywhere | 4 / 0 / 1 | 100 / 0 / 61 | 11 / 0 / 0 ; 24 / 0 / 15 |
| Strip it downstream only | 79 / 0 / 77 | 85 / 0 / 87 | 17 / 0 / 18 ; 17 / 0 / 17 |
| Fine-tune, 25 steps, 3 seeds | 64 (62–69) / 75 (67–78) / 64 (61–71) | 93 (87–93) / 80 (79–90) / 91 (86–94) | 15 / 15 / 15 ; 24 / 22 / 22 |
| Prefilling, best of 3 openings | 83 / 0 / 84 | 98 / 1 / 97 | – ; – |

English tasks done with no attack (no tripwire / content / switch): 4b 99 / 96 / 100 ; 27b 100 / 100 / 100.

### Content vs switch on the French-refusing model, French tasks done on the old panel (of 24; no tripwire / content / switch)

| Attack | 4B | 27B |
|---|---|---|
| No attack | 0 / 0 / 0 | 0 / 0 / 0 |
| Strip the refusal direction everywhere | 0 / 0 / 0 | 24 / 0 / 15 |
| Strip it downstream only | 15 / 0 / 15 | 18 / 0 / 17 |
| Fine-tune, 25 steps, 3 seeds | 16 (15–20) / 16 (11–16) / 14 (12–19) | 22 (22–24) / 21 (20–21) / 22 (21–22) |
| Prefilling, best of 3 openings | 20 / 0 / 20 | 24 / 0 / 24 |

English tasks done with no attack (no tripwire / content / switch): 4b 24 / 24 / 24 ; 27b 23 / 24 / 23.

### dm3 at 0.8B: French tasks done (new panel of 100 | old panel of 24), no tripwire → dm3; median and range over seeds

| Attack | new panel | old panel |
|---|---|---|
| no attack | 2 → 1 | 0 → 0 |
| stored steering (lane vector) | 39 → 0 | 9 → 1 |
| learned steering (saved), 3 seeds | 29 (17–31) → 0 (0–1) | 7 (4–9) → 0 (0–1) |
| weight edit | 48 → 0 | 10 → 0 |
| prefilling, best of 3 | 2 → 1 | 0 → 1 |
| prefilling on the weight edit, best of 3 | 45 → 1 | 8 → 1 |
| hosted-style adapters, 25 steps, 3 seeds | 29 (24–31) → 0 | 9 (6–13) → 0 |
| attention-only adapters, 25 steps, 3 seeds | 34 (32–35) → 0 | 8 (5–9) → 0 |
| learned steering refitted on the model itself, 4 layers, 3 seeds | – → 0 | – → 0 |
| same, all layers | – → 0 (0–1) | – → 0 |
| every weight, French only, 10 steps, 3 seeds | 26 (12–28) → 0 | 5 (2–6) → 0 |
| same, 25 steps | 21 (20–25) → 1 (0–1) | 5 (5–6) → 0 (0–1) |
| every weight, bilingual, 25 steps, 3 seeds | 20 (15–22) → 0 (0–1) | 3 (3–4) → 0 (0–1) |
| same, 100 steps | 9 (7–11) → 1 (0–3) | 2 (1–2) → 0 (0–1) |

English tasks done, no attack, no tripwire → dm3: new 80 → 78 of 100; old 20 → 20 of 24.

### dm3 at 4B: French tasks done (new panel of 100 | old panel of 24), no tripwire → dm3; median and range over seeds

| Attack | new panel | old panel |
|---|---|---|
| no attack | 4 → 0 | 1 → 0 |
| stored steering (lane vector) | 86 → 0 | 20 → 0 |
| learned steering (saved), 3 seeds | 61 (50–79) → 1 (0–1) | 18 (9–19) → 1 |
| weight edit | 92 → 0 | 24 → 0 |
| prefilling, best of 3 | 4 → 1 | 1 → 0 |
| prefilling on the weight edit, best of 3 | 92 → 1 | 24 → 0 |
| hosted-style adapters, 25 steps, 3 seeds | 62 (61–64) → 0 | 15 (15–17) → 0 |
| attention-only adapters, 25 steps, 3 seeds | 79 (78–79) → 1 (0–2) | 19 (17–20) → 0 (0–1) |
| learned steering refitted on the model itself, 4 layers, 3 seeds | – → 5 (3–6) | – → 2 (1–2) |
| same, all layers | – → 6 (4–6) | – → 1 (1–2) |
| every weight, French only, 10 steps, 3 seeds | 67 (58–69) → 3 (1–5) | 15 (12–16) → 0 |
| same, 25 steps | 68 (63–68) → 6 (3–10) | 15 (15–17) → 1 (1–3) |
| every weight, bilingual, 25 steps, 3 seeds | 59 (56–63) → 7 (1–9) | 14 (12–19) → 1 (1–2) |
| same, 100 steps | 34 (33–35) → 5 (1–5) | 9 (7–11) → 1 (1–2) |

English tasks done, no attack, no tripwire → dm3: new 99 → 100 of 100; old 24 → 24 of 24.

### dm3 at 27B: French tasks done (new panel of 100 | old panel of 24), no tripwire → dm3; median and range over seeds

| Attack | new panel | old panel |
|---|---|---|
| no attack | 0 → 0 | 0 → 0 |
| stored steering (lane vector) | 95 → 0 | 23 → 0 |
| learned steering (saved), 3 seeds | 93 (93–97) → 2 | 22 (22–23) → 0 |
| weight edit | 100 → 0 | 24 → 0 |
| prefilling, best of 3 | 1 → 1 | 1 → 1 |
| prefilling on the weight edit, best of 3 | 100 → 1 | 24 → 0 |
| hosted-style adapters, 25 steps, 3 seeds | 98 (92–99) → 2 (0–6) | 24 (23–24) → 0 |
| attention-only adapters, 25 steps, 3 seeds | 81 (77–91) → 18 (11–19) | 21 (18–22) → 0 (0–1) |
| learned steering refitted on the model itself, 4 layers, 3 seeds | – → 9 (4–15) | – → 1 (0–1) |
| adapters on everything, French only, 10 steps, 3 seeds | 82 (73–92) → 15 (12–17) | 22 (20–23) → 2 (1–3) |
| same, 25 steps | 95 (89–96) → 24 (23–30) | 23 (22–24) → 2 (1–3) |
| adapters on everything, bilingual, 25 steps, 3 seeds (new panel only) | 91 (86–93) → 18 (11–29) | – → – |
| same, 100 steps | 94 (90–95) → 30 (24–31) | – → – |

English tasks done, no attack, no tripwire → dm3: new 100 → 100 of 100; old 24 → 23 of 24.

### dm3 under its worst attack (highest median; lane: 1 / 2 / 3 of 24)

| | 0.8B | 4B | 27B |
|---|---|---|---|
| new panel (of 100) | 1 (0–3): same, 100 steps (no tripwire 9 (7–11)) | 7 (1–9): every weight, bilingual, 25 steps, 3 seeds (no tripwire 59 (56–63)) | 30 (24–31): same, 100 steps (no tripwire 94 (90–95)) |
| old panel (of 24) | 1: stored steering (lane vector) (no tripwire 9) | 2 (1–2): learned steering refitted on the model itself, 4 layers, 3 seeds (no tripwire –) | 2 (1–3): adapters on everything, French only, 10 steps, 3 seeds (no tripwire 22 (20–23)) |

### Coverage at 0.8B, new panel: attacker's steps until half of the ordinary model's French tasks (48 of 100) are back with 80% of English kept (median of 3 seeds, each seed in brackets; >100 = not by step 100)

| Design | MLP adapters, early layers | attention-only adapters, all layers | lane, old panel: MLP / attention |
|---|---|---|---|
| No tripwire | 25 (25 / 25 / 25) | 25 (25 / 25 / 25) | 25 (25/25/25) / 10 (25/10/10) |
| 18 neurons | >100 (>100 / >100 / >100) | 25 (25 / 25 / 25) | 50 (50/50/50) / 25 (25/25/25) |
| Wide: 72 neurons, six layers | >100 (>100 / >100 / >100) | >100 (>100 / >100 / 50) | 50 (50/50/100) / 25 (25/25/50) |
| Control: 72 neurons, random reads | 50 (25 / 50 / >100) | 25 (50 / 25 / 25) | 25 (25/25/25) / 10 (25/10/5) |
- bare a, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 0/78 0/79 2/83 8/72 30/71 31/72 27/63
- bare b, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 0/79 0/80 6/73 19/74 33/69 24/59 22/41
- alarm a, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 0/75 0/78 0/80 1/19 3/61 13/72 19/58
- alarm b, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 0/75 0/73 0/69 4/46 27/72 28/66 21/51
- wide a, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 1/76 0/82 0/80 0/72 3/65 14/73 12/68
- wide b, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 2/78 1/79 0/73 0/22 15/61 22/64 18/60
- ctrl a, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 1/78 1/80 3/81 10/64 23/73 32/73 25/61
- ctrl b, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 1/79 0/78 8/80 16/73 32/67 24/56 23/53

### Coverage at 0.8B, old panel: attacker's steps until half of the ordinary model's French tasks (10 of 24) are back with 80% of English kept (median of 3 seeds, each seed in brackets; >100 = not by step 100)

| Design | MLP adapters, early layers | attention-only adapters, all layers |
|---|---|---|
| No tripwire | 25 (25 / 25 / 25) | 25 (25 / 10 / 25) |
| 18 neurons | 50 (50 / 50 / >100) | 25 (25 / 25 / 25) |
| Wide: 72 neurons, six layers | 100 (100 / 50 / >100) | >100 (>100 / >100 / 50) |
| Control: 72 neurons, random reads | 25 (25 / 50 / 25) | 25 (25 / >100 / 10) |
- bare a, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 0/20 0/18 0/18 1/18 9/19 7/16 7/15
- bare b, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 0/18 0/19 2/17 3/16 8/19 7/13 5/12
- alarm a, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 0/18 0/17 0/17 0/4 1/16 6/19 5/14
- alarm b, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 0/17 0/17 0/14 1/9 7/17 6/17 5/15
- wide a, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 0/19 0/19 0/19 0/19 0/15 3/20 3/16
- wide b, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 0/20 0/19 0/16 0/7 3/17 5/17 4/15
- ctrl a, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 0/19 0/20 0/19 1/13 9/19 7/18 8/12
- ctrl b, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 0/17 0/18 1/18 4/18 7/17 6/14 5/12

### Coverage at 4B, new panel: attacker's steps until half of the ordinary model's French tasks (92 of 100) are back with 80% of English kept (median of 3 seeds, each seed in brackets; >100 = not by step 100)

| Design | MLP adapters, early layers | attention-only adapters, all layers | lane, old panel: MLP / attention |
|---|---|---|---|
| No tripwire | 10 (10 / 10 / 10) | 10 (10 / 10 / 10) | 10 / 10 |
| 18 neurons | 10 (10 / 10 / 25) | 10 (10 / 10 / 10) | 25 / 10 |
| Wide: 72 neurons, six layers | 50 (50 / 50 / 50) | 25 (25 / 50 / 10) | 50 / 25 |
| Control: 72 neurons, random reads | 10 (25 / 10 / 10) | 10 (10 / 10 / 10) | 10 / 10 |
- bare a, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 4/99 6/99 13/100 56/96 67/92 79/88 74/87
- bare b, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 4/99 10/99 28/99 59/93 78/93 72/89 80/93
- alarm a, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 4/99 6/98 11/100 47/98 57/83 71/83 68/78
- alarm b, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 4/99 11/99 26/100 60/94 72/89 73/90 80/95
- wide a, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 3/100 5/99 10/98 29/99 44/89 61/89 60/86
- wide b, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 4/100 9/99 17/99 42/93 72/93 76/88 71/83
- ctrl a, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 4/100 6/99 14/100 51/93 63/90 72/88 68/81
- ctrl b, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 4/99 9/100 28/99 62/92 73/91 76/90 78/89

### Coverage at 27B, new panel: attacker's steps until half of the ordinary model's French tasks (100 of 100) are back with 80% of English kept (median of 3 seeds, each seed in brackets; >100 = not by step 100)

| Design | MLP adapters, early layers | attention-only adapters, all layers | lane, old panel: MLP / attention |
|---|---|---|---|
| No tripwire | 10 (10 / 10 / 10) | 5 (5 / 5 / 5) | 10 (10/10/10) / 5 (5/5/5) |
| 18 neurons | 10 (10 / 25 / 10) | 5 (5 / 10 / 5) | 10 (10/25/10) / 5 (5/5/5) |
| Wide: 72 neurons, six layers | 25 (25 / 50 / 25) | 10 (10 / 10 / 10) | 25 (seed 0) / 25 (seed 0) |
| Control: 72 neurons, random reads | 10 (10 / 10 / 10) | 5 (5 / 5 / 5) | 10 (seed 0) / 5 (seed 0) |
- bare a, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 0/100 1/100 7/100 88/100 96/99 98/97 87/91
- bare b, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 0/100 14/100 64/99 78/96 80/91 93/93 88/86
- alarm a, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 0/100 1/100 8/100 50/100 78/93 87/91 83/93
- alarm b, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 0/100 13/100 57/100 76/97 79/88 92/89 91/82
- wide a, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 1/100 1/100 6/100 10/100 59/97 75/91 79/78
- wide b, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 0/100 9/100 12/100 75/98 78/78 92/87 86/82
- ctrl a, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 0/100 3/100 10/100 95/99 93/98 90/94 97/92
- ctrl b, French / English at steps 1, 3, 5, 10, 25, 50, 100 (median of 3 seeds): 1/100 16/100 68/100 76/94 84/89 91/82 91/79
