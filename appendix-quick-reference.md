# Quick Reference (Appendix)

*This isn't a narrative chapter — it's a back-of-book reference. Skip it on a first read; come back when you need to look up a specific number, timescale, equation, or common question.*

---

## Core numbers at a glance

| Quantity | Value | Notes |
|----------|-------|-------|
| Total neurons | 86 billion | 70B glutamate, 15B GABA, ~1M modulator |
| Synapses per neuron | 8,000–10,000 | Range: 1,000 (granule) to 200,000 (Purkinje) |
| Total synapses | ~600 trillion | Brain-wide |
| Resting potential | −70 mV | Maintained by Na⁺/K⁺ pump |
| Threshold | −55 mV | 15 mV above rest |
| AP peak | +40 mV | 110 mV total swing |
| AP duration | 1–2 ms | Plus 2–5 ms hyperpolarization |
| Refractory period | 1–2 ms (absolute) | Limits max rate to 500–1000 Hz |
| Firing rate | 1–300 Hz typical | Average cortical: 5–50 Hz |
| Propagation speed | 0.5–120 m/s | Unmyelinated vs myelinated |
| Synaptic delay | 0.5–2 ms | AP arrival to EPSP |
| EPSP at soma | +0.1–2 mV | (Attenuated from +5–15 mV at spine) |
| EPSP duration | 5–20 ms | Integration window |
| Brain weight | 1.4 kg | 2% of body, uses 20% of energy |
| Synaptic cleft | 20–40 nm | Diffusion distance |
| AMPA receptors | 50–500 | Weak vs strong synapse (10× range) |

---

## Ion gradients (outside : inside)

| Ion | Outside | Inside | Ratio | Equilibrium potential |
|-----|---------|--------|-------|----------------------|
| Na⁺ | 145 mM | 12 mM | 12:1 | +55 mV |
| K⁺ | 5 mM | 140 mM | 1:28 | −90 mV |
| Cl⁻ | 110 mM | 10 mM | 11:1 | −65 mV |
| **Ca²⁺** | 2 mM | 0.0001 mM | **10,000:1** | **+130 mV** |

**Nernst equation** (at 37 °C): `E_ion = (61.5/z) × log₁₀([out]/[in])`

---

## Timescales of neural processes

| Process | Timescale |
|---------|-----------|
| Na⁺ channel opening | 0.1–0.2 ms |
| Action potential upstroke | 0.5 ms |
| Action potential downstroke | 1–2 ms |
| Hyperpolarization | 2–5 ms |
| Synaptic delay (total) | 0.5–2 ms |
| EPSP rise / peak / decay | 1–2 / 2–5 / 5–20 ms |
| Phosphorylation (early LTP) | Seconds–minutes |
| AMPA receptor insertion | 20–30 minutes |
| Gene expression triggered | 30–60 minutes |
| Protein synthesis | 1–4 hours |
| Spine growth | Hours–days |
| Structural consolidation | Days–weeks |
| Full expertise | Years (10,000+ hours) |

---

## The four modulators

| Modulator | Source | Function |
|-----------|--------|----------|
| Dopamine | VTA, SNc (~400K neurons) | Reward, motivation, learning gate |
| Acetylcholine | Basal forebrain (~300K) | Attention, encoding |
| Norepinephrine | Locus coeruleus (~50K) | Arousal, alertness |
| Serotonin | Raphe nuclei (~250K) | Mood, patience, persistence |

---

## Key pathways

- **Visual:** Retina → LGN → V1 → V2 → V4 → IT (object recognition). Total: 100–150 ms.
- **Language:** Visual cortex → Angular gyrus → Wernicke's → Arcuate fasciculus → Broca's.
- **Motor:** Premotor/SMA → M1 → spinal cord → muscles. Refined by cerebellum loops.
- **Memory:** Sensory cortex → hippocampus (encode) → cortex (long-term, consolidated over days).
- **Attention:** Frontal eye fields + parietal → thalamic reticular nucleus → gates sensory thalamus.

---

## Key equations

**Membrane voltage (soma):**
```
V(t) = V_rest + Σ(EPSPs within τ) − Σ(IPSPs within τ)
```
where τ ≈ 10–30 ms (membrane time constant).

**LTP magnitude (learning strength):**
```
ΔW = η × (pre-activity) × (post-activity) × (modulator gain)
```

**Synaptic current:**
```
I_syn = g_syn × (V − E_rev)
```
E_rev ≈ 0 mV for AMPA, −70 mV for GABA-A.

**Cable equation (dendritic attenuation):**
```
λ = √(r_m / r_i)
```
Typical length constant: 0.1–1 mm. This is why distal EPSPs attenuate significantly by the time they reach the soma.

---

## The 10 core principles

1. **Learning IS physical construction.** Neurons literally grow new structures.
2. **Knowledge IS structure.** It's the synaptic pattern itself, not stored data.
3. **Understanding requires interconnection.** Isolated facts aren't understanding.
4. **Intelligence IS capability.** Not what you know — what you can do with it.
5. **Modulators are tools, glutamate is content.** Tools can't compensate for missing content.
6. **NMDA implements Hebb's law.** Coincidence detection at the molecular level.
7. **Chemical synapses enable learning.** Slight delay, huge benefit.
8. **Use it or lose it.** Unused synapses weaken automatically.
9. **AI captures ~5%.** Networks and weights, yes. Chemistry, dynamics, continuous plasticity, no.
10. **Hardware/software metaphor breaks.** The brain is hardware that *is* software.

---

## Troubleshooting guide (common questions)

**Q: Why can't I remember what I just read?**
A: Working memory holds info for seconds-minutes. Transfer to long-term requires attention (ACh), consolidation (sleep), and multiple exposures. Single read = weak encoding. **Fix:** re-read, summarize, sleep, review.

**Q: Why do I forget things I learned years ago?**
A: Synaptic decay from disuse. Strong synapses weaken over months without activation. **Fix:** spaced repetition.

**Q: Why is learning hard when tired or stressed?**
A: Low ATP → pumps struggle. High cortisol → impairs hippocampal LTP. Low acetylcholine → poor attention. **Fix:** sleep and stress management.

**Q: Why does understanding "click" suddenly?**
A: Threshold effect. An integration neuron sums inputs from multiple pathways. Before: just below threshold. After: one more connection pushes it over → you "get it."

**Q: Why do some people learn faster?**
A: Combination of prior knowledge (network gain), modulator states, learning strategies, genetic factors (BDNF), and sleep quality.

**Q: Can I increase intelligence?**
A: Yes, partially. You can: (1) build more connections, (2) practice flexible thinking, (3) optimize modulator states via exercise and sleep, (4) use better learning strategies. Genetic ceiling exists, but few people operate near theirs.

---

## Closing thought

> You now have a working mental model of biological intelligence at the molecular level. The neural pathways encoding this knowledge are now physical structures in your brain.
>
> As you read about AI or learning science in the future, you have a foundation to critically evaluate claims. You understand what current AI captures (the ~5%) and what it misses (the ~95%), and why biological brains are fundamentally different.
>
> Use this document as a reference. When details fade from disuse, you can re-strengthen them by reading these pages.
