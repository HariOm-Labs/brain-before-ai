# Chapter 1: The Biological Neuron

## The neuron as a computational unit

A single neuron is not a simple switch. It's a sophisticated computational device with roughly 15 distinct structural components, each playing a critical role. Artificial neural networks model a neuron as a simple mathematical function (weighted sum → activation). Biological neurons are molecular computers with capabilities we're only beginning to understand.

---

## The shape of a neuron

Before the components, here's the basic anatomy in one picture. Information flows **downward** through this diagram:

```
          \  |  /  /  |  \            ← DENDRITES
           \ | /  /   |   \             (input branches,
            \|/ /     |    \            each dotted with
         ___* *_______|_____\___        tiny "spines" that
        |   \ /       |     /   |       receive signals)
        |    X        |    /    |
        |   / \       |   /     |
         \_/___\______|__/______/
                   |
                ___|___
               /       \
              |   SOMA  |      ← CELL BODY (sums all
              |  (cell  |         inputs; decides whether
              |  body)  |         to "fire" a spike)
               \___|___/
                   |              ← AXON HILLOCK
                   |                 (where the spike starts)
                   |
                   |  ← AXON (output wire)
             ======|======       ← myelin insulation
                   |                (speeds up the spike)
             ======|======       ← Node of Ranvier
                   |                (where spike regenerates)
             ======|======
                   |
            ___ ___|___ ___
           /   X   X   X   \    ← AXON TERMINALS
          /    |   |   |    \      (tiny "post offices" that
         *     *   *   *     *     release neurotransmitter
              | |  | |  | |         into the next neuron)
              ↓ ↓  ↓ ↓  ↓ ↓
         (signals to other neurons)
```

Keep this picture in mind as we go through each component in detail.

---

## A synapse, zoomed in

If we take one of those axon terminals above and zoom in a thousand-fold, we see the actual meeting point between two neurons — the **synapse**:

```
    ┌──────────────────────────────────┐
    │      PRESYNAPTIC TERMINAL        │   ← sending neuron
    │       (from sender neuron)       │
    │                                  │
    │     ● ● ●    ← vesicles          │
    │    ● ● ● ●     (each holds       │
    │     ● ● ●      ~10,000           │
    │                neurotransmitter  │
    │      ▼ ▼ ▼     molecules)        │
    │   ┌─┘ │ │                        │
    │   │  ┌┘ │   Ca²⁺ channels open → │
    │   │  │  └─  vesicles fuse →      │
    │   └──┴─┴──  contents released    │
    ├──────────────────────────────────┤
    │  ░ ░ ░ SYNAPTIC CLEFT ░ ░ ░     │   ← 20–40 nanometer gap
    │   ░   ● ● neurotransmitter   ░   │     (the chemical step)
    │  ░ ●   molecules diffusing   ░ ●  │
    │   ░     ● across the gap     ░    │
    ├──────────────────────────────────┤
    │   ▲ ▲ ▲ ▲ ▲                      │
    │   │ │ │ │ │                      │
    │   R R R R R   ← receptors        │
    │   │ │ │ │ │     (AMPA, NMDA)     │
    │   └─┴─┴─┴─┘     on the spine     │
    │                                  │
    │   ┌──────────────┐               │
    │   │ POSTSYNAPTIC │   ← receiving │
    │   │   MEMBRANE   │     neuron    │
    │   │ (dendritic   │               │
    │   │    spine)    │               │
    │   └──────────────┘               │
    └──────────────────────────────────┘

    Learning happens HERE.
    A weak synapse has ~50 receptors.
    A strong (learned) synapse has ~500.
```

The entire drama of learning — strengthening, weakening, remembering, forgetting — happens at these tiny gaps. Full mechanism in [Chapter 3](03-synaptic-transmission.md).

---

## The 15 components

### 1. Dendrites — the input network
- **Structure:** 5–7 main branches per neuron, each branching 10–20 times into a tree-like arbor. Total surface area: ~10,000–20,000 µm².
- **Function:** Receive input from thousands of other neurons. Each branch does *local* computation before sending signals to the soma. Not passive wires — active computing elements with voltage-gated channels that can generate dendritic spikes independently.
- **Specialization:** Branches specialize over time. One branch may house physics knowledge while another houses language.
- **Numbers:** ~12–15 primary dendrites, ~150–300 secondary branches, ~5,000–7,000 segments per pyramidal neuron.

### 2. Dendritic spines — learning sites
- **Structure:** Tiny mushroom-shaped protrusions (1–2 µm long) emerging from dendrites. Each contains actin cytoskeleton, receptors (AMPA, NMDA), scaffolding proteins, sometimes mitochondria.
- **Function:** Primary sites of learning. Each spine = one synapse = one learning unit. Narrow neck creates a biochemical compartment, so calcium signals stay confined to the individual spine.
- **Plasticity:** New spines form in hours during learning. Stabilize over days-weeks. Musicians have ~40% more spines in motor cortex. London taxi drivers have enlarged hippocampi.
- **Numbers:** 2,000–5,000 spines per cortical neuron. 5–15 spines per 10 µm of dendrite.

### 3. Synapses — connection points
- **Structure:** A three-part junction: presynaptic terminal, 20–40 nm synaptic cleft, postsynaptic density (a molecular machine containing ~1,000–2,000 proteins).
- **Function:** Signal transmission point. Converts electrical → chemical → electrical. The chemical gap is what enables **modulation** — strengthening (LTP), weakening (LTD), or elimination.
- **Types:** Glutamate (80–85%, excitatory), GABA (15–20%, inhibitory), modulator (<1%), peptide (rare).
- **Strength range:** Weak synapse has ~50 AMPA receptors, strong has ~500 — a 10× range built through learning.
- **Scale:** ~8,000–10,000 input synapses and 8,000–12,000 output synapses per neuron. Brain total: ~100 trillion synapses.

### 4. Soma (cell body) — integration center
- **Structure:** 10–30 µm diameter. Contains nucleus plus all cellular machinery. Membrane studded with ion channels, receptors, pumps, and transporters.
- **Function:** **Global integration.** Sums all dendritic inputs (thousands of EPSPs and IPSPs arriving millisecond-by-millisecond). If voltage reaches threshold (–55 mV), triggers an action potential. This is THE computational decision: fire or don't fire.
- **Membrane properties:** Resting potential –70 mV (maintained by Na⁺/K⁺ pump). Time constant 10–30 ms.
- **Key point:** Real-time computation happens here (milliseconds). The nucleus does NOT compute — it does gene expression (hours-days).

### 5. Nucleus — long-term control
- **Structure:** 6–10 µm sphere containing DNA (3 billion base pairs), transcription machinery.
- **Function:** **Long-term structural changes** via gene expression. Repeated learning triggers CREB (a transcription factor), which turns on genes for AMPA receptors, scaffolding proteins, and actin.
- **Timeline:** Immediate early genes activate within 15–30 min. Structural proteins 2–4 hours later. Protein synthesis 4–12 hours. Physical spine growth visible after 12–24 hours. **This is why sleep matters** — gene expression and protein synthesis happen during sleep.
- **Critical distinction:** The nucleus responds to *patterns* of activity by changing gene expression. It doesn't do real-time computation.

### 6. Axon — output cable
- **Structure:** A single long projection. Length from 0.1 mm (local interneurons) up to over 1 meter (motor neurons to the foot). Diameter 0.2–20 µm.
- **Function:** Carries action potentials from soma to terminals at 0.5–2 m/s (unmyelinated) up to 80–120 m/s (myelinated). Signals propagate without loss — spikes regenerate at each point.
- **Axon hillock:** The initiation site for action potentials. Has the lowest threshold and highest density of voltage-gated Na⁺ channels (50–100/µm²).
- **Transport:** Axon can't make proteins locally. Kinesin (forward) and dynein (back) transport cargo along microtubules at 1–400 mm/day.

### 7. Myelin sheath — insulation for speed
- **Structure:** Fatty wrapping formed by oligodendrocytes (CNS) or Schwann cells (PNS). 200–1000 µm segments separated by 1–2 µm Nodes of Ranvier.
- **Function:** Speeds up propagation 10–100× via **saltatory conduction** — the spike "jumps" between nodes rather than propagating continuously.
- **Why it matters:** Without myelin, a signal across 15 cm of human cortex would take 150–300 ms. With myelin: 2–8 ms.
- **Development:** Continues through age 20–25. Prefrontal cortex myelinates last — this is partly why teenagers have "slower" impulse control.
- **Disease:** Multiple sclerosis is myelin degradation — signals slow or fail.

### 8. Axon terminals — transmission sites
- **Structure:** Bulbous endings (0.5–2 µm) at axon tips. Each contains 100–200 synaptic vesicles, active zones (release sites), voltage-gated Ca²⁺ channels, mitochondria (20–40% of terminal volume).
- **Function:** Neurotransmitter release. When an action potential arrives: terminal depolarizes → Ca²⁺ channels open → Ca²⁺ floods in → vesicles fuse with membrane → 5,000–10,000 neurotransmitter molecules released into the cleft. Total time: 0.5–1 ms.
- **Orphan terminals:** ~15–25% of terminals are "orphans" — they exist but aren't currently forming functional synapses. This is reserve capacity for future learning.

### 9. Ion channels — molecular switches
- **Types:** Voltage-gated (open based on voltage), ligand-gated (open when neurotransmitter binds), leak (always open).
- **Key channels:** Na⁺ (upstroke of action potential), K⁺ (repolarization), Ca²⁺ (triggers neurotransmitter release and learning), Cl⁻ (inhibition via GABA).
- **Na⁺ channel details:** Opens at –55 mV (in 0.1 ms), inactivates at +30 mV (in 0.5 ms). The inactivation creates the refractory period (1–2 ms), which limits firing rate to ~500–1000 Hz.
- **Scale:** ~10–100 million ion channels per neuron. Each channel passes 1–10 million ions per second when open.

### 10. Neurotransmitters — chemical messengers
- **Glutamate:** Main excitatory transmitter (80–85% of synapses). Removed from cleft by astrocyte transporters.
- **GABA:** Main inhibitory transmitter (15–20%). Opens Cl⁻ channels → hyperpolarization.
- **Modulators:** Dopamine (reward), acetylcholine (attention), norepinephrine (arousal), serotonin (mood). Fewer than 1% of neurons but project widely — one dopamine neuron can influence 100,000+ cortical neurons. ([Chapter 6](06-neuromodulation.md) covers these in depth.)
- **Release quantal:** Each vesicle = 5,000–10,000 molecules = one "quantum". Weak synapse releases 0–1 quanta; strong synapse releases 5–10.

### 11. Receptors — signal catchers
- **Ionotropic** (fast, 1–5 ms): ligand-gated ion channels like AMPA, NMDA, GABA-A.
- **Metabotropic** (slow, 10–100 ms, can last minutes): G-protein coupled. Most modulator receptors are metabotropic.
- **AMPA receptors:** Glutamate-gated Na⁺ channels. 50–500 per synapse. **This is what changes during learning** — more AMPA = stronger synapse.
- **NMDA receptors:** Glutamate-gated Ca²⁺ channels — but require BOTH glutamate AND depolarization (Mg²⁺ block removed by voltage). This makes them **coincidence detectors** — the molecular implementation of Hebb's law. (Covered in detail in [Chapter 4](04-learning-mechanisms.md).)

### 12. Mitochondria — power plants
- Generate ATP via oxidative phosphorylation. Each glucose → 30–32 ATP.
- ATP powers: Na⁺/K⁺ pump (40% of brain ATP), Ca²⁺ pumps, neurotransmitter synthesis, protein synthesis.
- Concentrated at axon terminals (20–40% of volume), Nodes of Ranvier, and active dendritic spines.
- Brain uses 20% of body's energy despite being 2% of weight — ~20 Watts.

### 13–15. Supporting structures
- **Endoplasmic reticulum:** Rough ER makes proteins; smooth ER handles Ca²⁺ storage. Expands in dendrites during learning.
- **Cytoskeleton:** Microtubules (transport highways), neurofilaments (structure), actin (dynamic, critical in spines). Blocking actin blocks learning.
- **Motor proteins:** Kinesin, dynein, myosin — the delivery trucks.

---

## The complete information flow

Here's how a signal travels through a single neuron, end to end:

### Phase 1: Input reception (dendrites & spines)
1. Presynaptic terminal releases glutamate (5,000–10,000 molecules).
2. Glutamate diffuses across the 20–40 nm cleft in 0.1–0.5 ms.
3. Binds AMPA receptors on a dendritic spine.
4. Na⁺ flows in → spine depolarizes by +5 to +15 mV (the EPSP).
5. EPSP spreads through spine neck → dendrite shaft, attenuating with distance.

**Local dendritic computation:** Multiple spines on the same branch sum their EPSPs. If the local sum is large enough, the branch generates a *dendritic spike* that amplifies the signal. Different branches compute independently — like multi-core processing.

### Phase 2: Global integration (soma)
The soma performs a weighted sum:
```
V(soma) = V(rest) + Σ(EPSPs) − Σ(IPSPs)
```
- Integration window: 10–30 ms.
- Near inputs have more influence than distal ones.
- If V ≥ –55 mV → fire.

**Example:** Start at –70 mV. 500 weak synapses distributed over 20 ms contribute +15 mV. 100 inhibitory synapses subtract 5 mV. Final: –60 mV. Below threshold — doesn't fire. One more good input (+5 mV) and it would.

### Phase 3: Action potential initiation (axon hillock)
- Threshold reached at –55 mV.
- Na⁺ channels open (the axon hillock has the densest concentration in the neuron).
- Na⁺ floods in: voltage shoots to +40 mV in 0.5 ms.
- Self-propagating wave travels down the axon.

### Phase 4: Propagation (axon & myelin)
- **Unmyelinated:** Continuous regeneration, 0.5–2 m/s.
- **Myelinated:** Saltatory conduction — spike jumps node-to-node at 10–120 m/s.

### Phase 5: Terminal activation & release
- AP arrives at terminal → Ca²⁺ channels open.
- Ca²⁺ floods in (10,000× gradient!).
- Vesicles fuse via the SNARE complex.
- Neurotransmitter spills into cleft.
- Total time from AP arrival to next-neuron binding: 0.5–1 ms.

### Phase 6: Cycle repeats
The receiving neuron becomes the sending neuron for the next step in the chain. One thought involves millions of these cycles happening in coordinated patterns across the brain.

---

## Key takeaway

> Every thought, every memory, every moment of understanding involves billions of precisely-timed molecular events. When you learn something new, thousands of neurons synchronize this process, strengthen their connections via the calcium cascade, synthesize new proteins, and permanently change your brain's physical structure.
>
> **Knowledge is not a metaphor. It is a pattern of strong synaptic connections, physically distributed across multiple brain regions.**
