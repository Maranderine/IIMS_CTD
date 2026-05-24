# Lecture Overview — Einführung in die Ozeanographie (WS 2025/26)

## Relevance for CTD/Glider Project

| Lecture | Date | Topic | Relevance |
|---------|------|--------|-----------|
| Vorlesung_01 | Oct 21, 2025 | Salinity, density ρ=ρ(T,S,p), equation of state, σ anomaly | **Essential** |
| Vorlesung_02 | Nov 4, 2025 | Stratification, buoyancy frequency N², mixed layer, thermocline, convection | **Essential** |
| Vorlesung_03 | Nov 18, 2025 | Equations of motion, hydrostatics, continuity | Background only |
| Vorlesung_04 | Nov 25, 2025 | Coriolis, geostrophic balance | Background only |
| Vorlesung_05 | Dec 9, 2025 | Ekman transport, Ekman pumping, coastal upwelling | Low relevance |
| Vorlesung_06 | Dec 16, 2025 | Thermal wind, dynamic method | Optional extension |
| Vorlesung_07 | Jan 6, 2026 | Sverdrup transport, wind-driven gyres | Low relevance |
| Vorlesung_08 | Jan 13, 2026 | Thermohaline circulation, heat/salt conservation | **Relevant (context)** |
| Vorlesung_09 | Jan 20, 2026 | Atlantic water masses: AABW, NADW, AAIW; T-S section plots | **Most relevant** |
| Vorlesung_10 | Jan 27, 2026 | Atlantic meridional overturning, AMOC | **Relevant (context)** |
| Vorlesung_11 | — | Western boundary currents, vorticity | Low relevance |
| Vorlesung_12 | — | Margules equation, density layer tilt | Low relevance |

## Priority Reading for CTD Project

1. **Vorlesung_01** — equation of state and σ = ρ − 1000 kg/m³; directly computed from glider data
2. **Vorlesung_02** — mixed layer, buoyancy frequency N²; core physics behind "density distribution structure"
3. **Vorlesung_09** — Atlantic T/S section plots, water mass identification (AABW, NADW, AAIW); most directly applicable
4. **Vorlesung_08 + 10** — thermohaline circulation context; useful for interpretation/discussion section of report

The dynamics lectures (03–07, 11–12) are not directly needed — they explain *why* the water moves, but the project task is to characterize *what the structure looks like*.


## minimum knowledge 

1. **Density, Temperature, Salinity**
Seawater density ρ is primarily controlled by T and S: colder and saltier water is denser. They don't contribute equally — salinity dominates in cold water, temperature dominates in warm water. The density anomaly σ₀ = ρ - 1000 is just a convenience to avoid writing 1027 kg/m³ everywhere.

2. **In-situ vs Conservative Temperature**
In-situ T is what the sensor measures. But when you compress water by bringing it to depth, it warms slightly (adiabatic heating) — so two water parcels at the same in-situ T at different depths aren't actually the same. Conservative Temperature (CT) removes this pressure effect, making parcels comparable regardless of depth. GSW's CT_from_t() does this conversion.

3. **Practical vs Absolute Salinity**
Practical Salinity (PSU) is measured from conductivity. Absolute Salinity (SA, g/kg) adds a small correction for regional differences in seawater composition (dissolved silica etc.). The difference is tiny (~0.17 g/kg) but matters for accurate density calculations. GSW's SA_from_SP() does this.

4. **Thermocline / Pycnocline / Halocline**
These are all depth layers where something changes rapidly:

Thermocline — sharp temperature decrease with depth
Halocline — sharp salinity change with depth
Pycnocline — sharp density increase with depth
In most of the ocean the pycnocline is driven mainly by the thermocline (warm surface, cold deep). They often overlap but aren't identical.

5. **Water Masses**
Large bodies of water with characteristic T-S properties, formed at the surface in specific regions and then subducted. Examples in your Atlantic data:

AAIW (Antarctic Intermediate Water) — fresh salinity minimum ~800 m
NADW (North Atlantic Deep Water) — salty, cold, ~2000 m
They retain their T-S signature as they spread, which is why the T-S diagram is so useful.

6. **T-S Diagram**
Plots Conservative Temperature vs Absolute Salinity for every measurement. Because T and S are conservative (they don't change unless mixing occurs), water masses appear as tight clusters. Mixing between two masses appears as a straight line between their T-S points. Isopycnals (lines of constant density) are overlaid as contours — the diagram immediately shows which water is denser and where mixing is happening.
