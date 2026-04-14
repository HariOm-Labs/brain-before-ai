# Chapter 2: Neural Communication

## The action potential — electrical signaling in detail

Neurons need to send signals over long distances (up to 1+ meter). Passive electrical signals decay with distance — useless for long-range communication. The solution: **action potentials** — self-regenerating electrical spikes that maintain full amplitude over any distance.

---

## The resting state

### Ion concentrations (the critical gradients)

| Ion | Outside | Inside | Ratio | Driving force |
|-----|---------|--------|-------|---------------|
| Na⁺ | 145 mM | 12 mM | 12:1 (out:in) | Wants to flow IN |
| K⁺ | 5 mM | 140 mM | 28:1 (in:out) | Wants to flow OUT |
| Cl⁻ | 110 mM | 10 mM | 11:1 (out:in) | Near equilibrium |
| **Ca²⁺** | 2 mM | 0.0001 mM | **10,000:1** | **Huge drive IN** |

### The Na⁺/K⁺ pump
These gradients don't maintain themselves. The Na⁺/K⁺-ATPase pump constantly runs:
- Pumps **3 Na⁺ out** for every **2 K⁺ in**.
- Uses 1 ATP per cycle, runs ~100 cycles/second.
- Consumes **40–70% of a neuron's ATP**.
- Without it: gradients collapse within minutes and the neuron dies. This is why oxygen deprivation kills neurons so fast.

---

## The action potential at a glance

Here's the shape of a single spike, plotted as voltage over time:

```
  Voltage
  (mV)
   +40 |           *
       |          * *
       |         *   *          ← Phase 3: Depolarization
       |        *     *           (Na⁺ rushes IN)
     0 |       *       *
       |      *         *
       |     *           *      ← Phase 4: Repolarization
       |    *             *       (K⁺ flows OUT)
   -55 |---*---------------*-------- threshold
       |  *                 *
   -70 |**  Phase 1          *  ← Phase 1: Rest (−70 mV)
       |    Rest              *
   -80 |                       ***   ← Phase 5: Hyperpolarization
       |                             (K⁺ slow to close, overshoot)
       |_______________________________________
        0      1      2      3      4      5   Time (ms)

       ⟵  Phase 2  ⟶  ⟵ refractory ⟶
       (crossing threshold)  (cannot fire again yet)
```

**The whole spike lasts 2–5 milliseconds.** Once it starts, it runs to completion — no partial spikes. Every spike is the same size, no matter how strong the triggering input. Information is encoded in *how often* spikes occur, not how big they are.

---

## The 6 phases of an action potential

### Phase 1: Resting potential (–70 mV)
- K⁺ leak channels dominate (slow outflow of K⁺).
- Ready to fire. Like a loaded spring — energy stored in ion gradients.

### Phase 2: Threshold (–55 mV)
- Excitatory inputs (EPSPs) push voltage up.
- Typically needs 50–200 synapses firing within a 10–30 ms window.
- At –55 mV, voltage-gated Na⁺ channels begin to open.
- Small Na⁺ influx → more depolarization → more channels open → **positive feedback**.
- Point of no return: ~–50 mV.

### Phase 3: Depolarization — the upstroke (+40 mV)
- Na⁺ channels open fully (opening time: 0.1 ms).
- Massive Na⁺ influx driven by combined ~130 mV electrochemical gradient.
- Voltage shoots from –55 to +40 mV in **0.5 ms**.
- Stops short of Na⁺'s theoretical equilibrium (+55 mV) because K⁺ channels are already starting to open.

### Phase 4: Repolarization — the downstroke
- Na⁺ channels **inactivate** at +30 mV (critical — stops the spike from running away).
- K⁺ channels (slower) are now fully open.
- K⁺ flows out, removing positive charge.
- Voltage falls: +40 → 0 → –70 mV in 1–2 ms.

### Phase 5: Hyperpolarization (–80 mV)
- K⁺ channels slow to close → membrane overshoots rest.
- **Absolute refractory period (1–2 ms):** neuron cannot fire again regardless of input. Na⁺ channels are still inactivated.
- **Relative refractory period (3–10 ms):** neuron *can* fire but needs a stronger stimulus.
- These periods limit max firing rate to 500–1000 Hz and enforce one-way propagation.

### Phase 6: Return to rest
- K⁺ channels close. Na⁺/K⁺ pump restores exact ion distributions.
- Full cycle: 2–5 ms. Can repeat at 5–500 Hz depending on neuron type.

---

## Propagation — how the spike travels

### Unmyelinated axons
- Spike regenerates continuously at every point.
- Adjacent region depolarizes → threshold → fires → propagates.
- Speed: 0.5–10 m/s (proportional to √diameter).

### Myelinated axons — saltatory conduction
- Myelin insulates the axon. Ion channels concentrated at **Nodes of Ranvier** (1–2 µm gaps every 1 mm).
- Spike "jumps" from node to node, skipping myelinated regions.
- Speed: 10–120 m/s — up to 100× faster.
- Also **energy-efficient**: only nodes use ATP.
- This is why **multiple sclerosis** (myelin degradation) is so devastating.

---

## Information coding

### The all-or-nothing principle
Every action potential has the same amplitude (~110 mV swing, –70 to +40 mV). Doesn't matter if threshold was barely reached or massively exceeded — the spike is always the same size. This is the brain's "digital" aspect.

### Information is encoded in firing frequency
| Stimulus | Typical firing rate |
|----------|--------------------|
| Light touch | 10 Hz |
| Moderate pressure | 50 Hz |
| Painful stimulus | 200+ Hz |
| Visual edge detection | 40–80 Hz |
| Motor command (sustained) | 10–50 Hz |
| Theoretical max | 500–1000 Hz |

Temporal patterns also matter — burst firing, regular firing, and irregular firing each carry different meaning to downstream neurons.

---

## Critical distinction: membrane vs nucleus

A common confusion: does the nucleus do the calculation? **No.** The membrane and the nucleus operate on completely different timescales with different jobs.

| Aspect | Membrane | Nucleus |
|--------|----------|---------|
| Timescale | Milliseconds | Hours–days |
| Function | Integration, firing decision, signal transmission | Gene expression, protein synthesis, structural consolidation |
| Mechanism | Ion channels, voltage changes | Transcription factors, mRNA, protein synthesis |
| Role | **Computation** | **Consolidation** |

**Analogy:** The membrane is the CPU doing calculations right now. The nucleus is the factory that builds more CPU capacity based on usage patterns.

The nucleus doesn't integrate inputs or decide whether to fire. It responds to *patterns* of membrane activity by changing gene expression to support those patterns long-term.

---

## Closing thought

> The action potential is one of evolution's most elegant inventions. Every time a thought crosses your mind, every time your finger twitches, every time a memory surfaces, some variation of this 2-millisecond electrical spike is firing millions of times across your brain — each one obeying the same physics: sodium in, potassium out, threshold reached, message sent.
>
> But the spike is only half the story. It carries a signal reliably from one end of a neuron to the other, but neurons don't touch. To turn that signal into something another neuron can receive — and to turn that handoff into something that can *change* with experience — the brain does something far stranger. It converts the electrical spike back into a chemical, sends it across a tiny gap, and lets the chemical re-ignite electricity on the other side.
>
> That handoff is where learning lives. [Chapter 3](03-synaptic-transmission.md) is about that handoff.
