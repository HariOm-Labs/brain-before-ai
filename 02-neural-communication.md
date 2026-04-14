# Chapter 2: How a Brain Cell Sends a Signal

*The 2-millisecond electrical spike that carries every thought you've ever had.*

> 📍 *In [Chapter 1](01-biological-neuron.md), you met the parts of a neuron — listener, decider, broadcaster. The decider's whole job is to fire a single 2-millisecond electrical spike when conditions are right. This chapter is about that spike: what it actually is, how it travels, and how the brain solved an engineering problem that pure physics couldn't.*

---

## The problem the brain had to solve

Imagine you need to send a message from one end of a one-meter-long wire to the other. You whisper it in. By the time it reaches the other end, the signal has faded into nothing.

That's the challenge a neuron faces. Some axons in your body are over a meter long (motor neurons reaching from your spinal cord to your toes). A simple electrical signal sent down such a fiber would decay within a few millimeters — useless.

Evolution's solution is one of biology's most elegant inventions: the **action potential**. A self-regenerating electrical spike that maintains full strength no matter how far it travels. It's how your toes know when your brain says "wiggle." It's how a thought becomes a movement. It's how everything in your nervous system communicates.

This chapter is about how that spike works — and why it's the foundation of every signal in your head.

---

## Before the spike: the loaded spring

A neuron at rest isn't really at rest. It's more like a loaded spring. Electrically primed. Ready.

The trick is in the **ion gradients** — the wildly unequal distributions of charged particles inside and outside the cell.

| Ion | Outside the cell | Inside the cell | Wants to flow |
|-----|------------------|-----------------|---------------|
| Sodium (Na⁺) | High (145 mM) | Low (12 mM) | **Inward** |
| Potassium (K⁺) | Low (5 mM) | High (140 mM) | **Outward** |
| Chloride (Cl⁻) | High (110 mM) | Low (10 mM) | Mostly stable |
| **Calcium (Ca²⁺)** | Modest (2 mM) | **Almost zero (0.0001 mM)** | **Powerfully inward** |

Notice that calcium gradient — **10,000 to 1.** Calcium is so depleted inside the neuron that when channels do open, it rushes in like water through a broken dam. This becomes important in Chapter 3 (it triggers neurotransmitter release) and Chapter 4 (it triggers learning).

These gradients don't maintain themselves. A protein called the **Na⁺/K⁺ pump** runs constantly, pushing 3 sodium ions out for every 2 potassium ions in, using one molecule of ATP each cycle. It runs about 100 cycles per second and burns through **40–70% of a neuron's total energy budget**.

Why care about the pump? Because if it stops, the gradients collapse within minutes and the neuron dies. **This is why oxygen deprivation kills brain cells so fast** — no oxygen, no ATP, no pump, no gradients, no neuron.

The whole system is poised. Energy is stored in those gradients like potential energy in a stretched spring. The spike is what happens when the spring releases.

---

## The spike, at a glance

Here's the shape of a single action potential — voltage on the vertical axis, time on the horizontal:

```
  Voltage
  (mV)
   +40 |           *
       |          * *
       |         *   *          ← Phase 3: Depolarization
       |        *     *            (Na⁺ rushes IN)
     0 |       *       *
       |      *         *
       |     *           *      ← Phase 4: Repolarization
       |    *             *        (K⁺ flows OUT)
   -55 |---*---------------*-------- threshold
       |  *                 *
   -70 |**  Phase 1          *  ← Phase 1: Rest (−70 mV)
       |    Rest              *
   -80 |                       ***   ← Phase 5: Hyperpolarization
       |                                (overshoot before recovery)
       |_______________________________________
        0      1      2      3      4      5   Time (ms)
```

**The whole thing lasts 2–5 milliseconds.** Once it starts, it runs to completion. There's no such thing as a half-spike. Every action potential is the same size, no matter how strong the input that triggered it.

This is the brain's "digital" aspect — fire or don't fire, full strength or nothing. Information is encoded not in the *size* of spikes but in **how often they happen and in what patterns**.

---

## The 6 phases — what's actually happening

Let's slow the spike down and watch one fire.

### Phase 1 — At rest (−70 mV)
The neuron sits at about −70 millivolts (the inside is more negative than the outside). Potassium leak channels are open, slowly bleeding K⁺ outward. The Na⁺/K⁺ pump compensates. Stable. Waiting. Loaded.

### Phase 2 — Crossing the threshold (−55 mV)
Excitatory inputs arrive through the dendrites. Each one nudges the voltage upward by a tiny amount. Most of these nudges decay before they accumulate. But occasionally, enough arrive close together — typically 50 to 200 synapses firing within 10–30 milliseconds — to push the voltage past **−55 mV**.

That's the threshold. Crossing it triggers something that can't be undone. **Voltage-gated sodium channels start to open.** A tiny trickle of sodium flows in. That trickle depolarizes the membrane slightly more. Which opens more sodium channels. Which lets in more sodium. Which opens more channels.

This is positive feedback. Once it starts, there's no stopping it. Around −50 mV, the system is committed. The spike has begun.

### Phase 3 — The upstroke (rising to +40 mV)
Sodium channels snap fully open. Sodium ions, driven by both the concentration gradient and the electrical pull, flood inward at staggering rates. The voltage shoots from −55 mV to **+40 mV in half a millisecond**.

The membrane has gone from negative to positive faster than almost any biological event. This is the spike's birth.

### Phase 4 — The downstroke (falling back)
At +30 mV, the sodium channels do something critical: **they inactivate.** Not just close — physically pinch shut, refusing to open again until the voltage drops well below threshold. Without this inactivation, the spike would run away forever.

Meanwhile, the slower potassium channels are now fully open. K⁺ flows outward (140 mM inside, 5 mM outside — strong outward push). Positive charge leaves the cell. Voltage falls: +40 → 0 → −70 in about 1–2 milliseconds.

### Phase 5 — Hyperpolarization (the undershoot)
The potassium channels are slow to close. So K⁺ keeps leaving even after voltage hits resting level. The cell briefly overshoots into more-negative-than-rest territory: about −80 mV.

This is the **refractory period**. During the absolute refractory phase (1–2 ms), the neuron *cannot* fire again no matter how strong the input — sodium channels are still inactivated. During the relative refractory phase (3–10 ms after that), it *can* fire but needs an unusually strong stimulus.

This refractory period serves two purposes: it limits how fast a neuron can fire (max ~1000 Hz) and it ensures the spike travels in only one direction down the axon. The bit of axon behind the spike is in refractory and can't fire again — so the spike has to keep moving forward.

### Phase 6 — Back to rest
Potassium channels finally close. The Na⁺/K⁺ pump restores exact ion balances. The neuron is back at −70 mV, loaded again, ready for the next one.

Total elapsed time: 2 to 5 milliseconds for a complete cycle. Some neurons can repeat this 500 times per second.

---

## How the spike travels — the speed problem

A spike born at the axon hillock has to reach the terminals. That distance can be huge. How does it propagate?

### Slow option: continuous regeneration
On unmyelinated axons, the spike regenerates at every adjacent point. Each tiny segment of membrane has to depolarize, fire, recover. It's like a row of dominoes, but slow. **Speed: 0.5–10 m/s.** Acceptable for short connections inside the cortex. Useless for the meter-long axon to your toe.

### Fast option: jumping through insulation
Most long axons are wrapped in **myelin** — a fatty insulation that prevents ion flow. The myelin doesn't allow spikes to fire under it. Instead, ion channels are clustered at tiny gaps between myelin segments, called **Nodes of Ranvier**, every 1–2 millimeters.

The spike "jumps" from one node to the next. It only has to fire at the nodes, not continuously. **Speed: 10–120 m/s — up to 100× faster.**

This is also dramatically more energy-efficient. Only the nodes use ATP. Vast stretches of axon stay quiet.

This is why **multiple sclerosis** is so devastating. MS destroys myelin. Without it, signals slow down, distort, or fail entirely. The neuron itself is fine — its messages just can't get there in time to be useful.

---

## How information is encoded

Every action potential is the same size. So how does the brain encode information about *what* the signal means?

**Frequency.** The number of spikes per second.

| Stimulus type | Typical firing rate |
|---------------|---------------------|
| Light touch on skin | ~10 Hz |
| Moderate pressure | ~50 Hz |
| Painful stimulus | 200+ Hz |
| Visual edge detection | 40–80 Hz |
| Motor command, sustained | 10–50 Hz |
| Theoretical maximum | ~1000 Hz |

A stronger input = more spikes per second. The brain reads frequency the way you'd read a Morse code: more dots per second = more urgency.

Beyond raw frequency, the *temporal pattern* also carries information. Burst firing (3–5 quick spikes followed by a pause) means something different than evenly-spaced firing. Multiple downstream neurons can decode the same axon's output differently based on how spikes are clustered in time.

---

## A common confusion: membrane vs nucleus

People sometimes assume the *nucleus* of the neuron is where decisions get made. It isn't. The **membrane** does real-time computation; the nucleus does long-term consolidation. Two completely different timescales, two completely different jobs:

| Aspect | Membrane | Nucleus |
|--------|----------|---------|
| **Timescale** | Milliseconds | Hours to days |
| **Job** | Integrate inputs, fire spikes | Express genes, build proteins |
| **Mechanism** | Ion channels, voltage changes | Transcription factors, mRNA |
| **Role** | Computation | Consolidation |

Think of the membrane as the CPU running calculations right now. The nucleus is the factory that builds more CPU capacity in response to usage patterns. They cooperate, but they don't do each other's jobs.

---

## Closing thought

> The action potential is one of evolution's most elegant inventions. Every time a thought crosses your mind, every time your finger twitches, every time a memory surfaces — some variation of this 2-millisecond electrical spike is firing millions of times across your brain. All of them obey the same physics: sodium in, potassium out, threshold reached, message sent.
>
> But the spike is only half the story.
>
> It carries a signal reliably from one end of a neuron to the other — but neurons don't touch. To turn that signal into something another neuron can receive, and to turn that handoff into something that can *change* with experience, the brain does something stranger and more remarkable. It converts the electrical spike back into a chemical, sends it across a tiny gap, and lets the chemical re-ignite electricity on the other side.
>
> That handoff is where learning lives. [Chapter 3](03-synaptic-transmission.md) is about that handoff.
