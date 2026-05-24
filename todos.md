## TODOS

## Preparation (before data arrives)
- [ ] Read Sensor-Driven preprint + TEOS-10 Primer (sections 1 and 2.1)
- [ ] ask professor: processing level (L0/L1/L2), file format, QC flags already applied?, thermal lag corrected?, which section he recommends
- [ ] Install gsw, cmocean, glidertools and verify notebook runs on dummy data
- [ ] literature research (CTD/glider analysis)
      priority: Sensor-Driven preprint > TEOS-10 Primer > Getting_Started (reference) > glider_data_processing
- [ ] gather information about glider, surrounding, recording time

## Week 1 — Data loading & first look
- [ ] Load data, understand variable names/units/fill values, replace dummy loader in notebook
- [ ] First raw plots: track map, T and S time series coloured by depth
- [ ] QC: filter NaNs, impossible values, surface startup noise, obvious spikes
- [ ] Dive segmentation: confirm dive_id assignment
- [ ] Write 1-paragraph "Data" description for report while it's fresh
- [ ] Compute SA, CT, σ₀ via gsw (SA_from_SP, CT_from_t, sigma0)
- [ ] Compute N² per dive (gsw.Nsquared)
- [ ] Compute mixed layer depth (gt.physics.mixed_layer_depth)
- [ ] Grid data onto regular depth × dive grid (gt.mapping.grid_data)
- [ ] Validation: check T/S values fall in expected Atlantic ranges for the latitude band

## Week 2 — Preprocessing & derived variables
- [ ] Profile plots: T, S, σ₀ vs depth for representative dives
- [ ] Section plots: T, S, σ₀ as 2D depth × latitude colormesh
- [ ] N² section: identify thermocline depth along transect
- [ ] T-S diagram with isopycnals: identify water masses (AAIW, NADW, AABW)
- [ ] MLD plot along transect
- [ ] Interpret findings: water masses present, mixed layer depth, thermocline, anomalies
- [ ] Draft Results + Interpretation/Discussion section

## Week 3 — Analysis & Report (deadline June 15/16)

- [ ] Write Introduction and Methods sections
- [ ] Assemble full report: Context → Data → Methods → Results → Interpretation
- [ ] Clean notebook: remove scratch cells, add markdown, confirm runs top-to-bottom on fresh kernel
- [ ] Build presentation slides (7 min): 1 context, 1 data/methods, 3-4 result figures, 1 conclusion
- [ ] Submit report + notebook (June 15)
- [ ] Presentation (June 16)
