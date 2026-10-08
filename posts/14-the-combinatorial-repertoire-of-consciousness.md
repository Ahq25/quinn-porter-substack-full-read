# The Combinatorial Repertoire of Consciousness

*Context Dependent Gating, Temporal Basin Compression, and Recursive Access*

- **Author:** Quinn Porter
- **Published:** October 2, 2026, 12:48 PM ET
- **URL:** https://ahq25.substack.com/p/the-combinatorial-repertoire-of-consciousness
- **Audience:** everyone (free, public)

---

An ordinary visual scene can contain several objects, movement, color, spatial relationships, remembered significance, bodily relevance, and the demands of a current task. The nervous system must respond to particular combinations of these features while remaining capable of responding differently when the context changes. The number of possible meaningful experiences is much larger than the number of individual types of sensory input.

[The Combinatorial Repertoire of Consciousness](https://philarchive.org/rec/PORTCR-5) proposes an organizational explanation for this variety. Relatively stable local gates can be recruited in many combinations. Their activity depends not only on what arrives now, but also on signal conjunctions, timing, the physical history carried by the system, and feedback from larger patterns of activity. Different sequences of gate activity can create different routes through the same finite physical network.

### A finite system with many possible routes

Consider a particular patch of red in a visual scene. It may be part of a traffic signal, a piece of fruit, a game, or an object remembered from childhood. The light entering the eye does not uniquely specify which of these relationships becomes relevant.

Other features and current conditions change how the signal participates. Shape and location may identify an object. A task may determine whether the color is important. Previous experience may associate the object with a specific action. An ongoing interpretation can alter which additional details are attended to next.

A gate is an effective condition that changes how one pattern of activity influences subsequent activity. It need not be a single neuron that is permanently either open or closed. A gate can be realized through nonlinear dendritic responses, combinations of synaptic input, state-dependent excitability, local circuits, or more distributed interactions.

If K gates each have two effective states, there are at most 2^K instantaneous binary combinations. Twenty-four binary gates have 2^24 = 16,777,216 formal patterns. The equation counts possible binary assignments; it does not imply that a particular circuit can reach every assignment, or that each reachable assignment corresponds to a distinct conscious experience.

The repertoire becomes larger still when the order of gate activations matters and when the same activation pattern leads to different outcomes depending on the state the system has retained.

### Biological precedents for selective combination

Adaptive immunity demonstrates how finite biological machinery can produce a large repertoire of possible recognitions. Immune cells assemble receptor variants through combinatorial genetic processes, and encounters with particular targets can select and expand specific cell populations. Later responses can depend on what earlier encounters changed.

This is a precedent for combinatorial generation, selective recruitment, and historical adaptation. It is not evidence that immunity and conscious perception share the same mechanism or that immune recognition is phenomenal.

Olfaction provides a different example within sensory processing. Odors can activate combinations of receptor types, and downstream activity can distinguish many conditions through the distributed pattern rather than the response of one dedicated detector. A finite collection of response channels supports a large space of discriminable combinations.

In the nervous system, mixed selectivity allows neurons and populations to respond differently to a feature depending on another feature, a rule, or a task condition. Dendritic nonlinearities permit combinations of inputs to produce effects that cannot be reduced to adding each input independently. Ongoing oscillatory phase can change the effectiveness of an arrival, while recurrent dynamics carry consequences of preceding states into the next decision.

These mechanisms provide physical candidates for the gate operations. They must still be connected to an integrated, temporally continuing organization before they explain particular experiential contents.

### Context changes the effect of the same arrival

The same incoming signal may produce different responses after a change in the network's retained state. A familiar sound during quiet rest can recruit one pattern of activity, while the same sound during a demanding task can recruit another. The stimulus is not the only relevant cause; present attention, learned associations, and the current population state also affect the response.

Retained history is physically represented in synaptic properties, adaptation, excitability, recurrent activity, neuromodulation, and other state variables. These carriers allow earlier events to shape later gating.

Timing adds a second source of selectivity. If the receiving network is oscillating, an input may arrive during a phase when it propagates strongly or during a phase when its effect is reduced. A collection of signals that arrives together may therefore be received differently from the same signals arriving separately.

These processes give a specific meaning to **history-dependent gating**. The gate is not a fixed label assigned by an observer; it is a condition within the dynamics that changes what the next state can become.

### The gate architecture

The paper represents the current neural state by x_t, an incoming signal by e_t, retained historical variables by h_t, relevant oscillatory phases by φ_t, and a preceding collective macrostate by M_(t−1).

Each candidate gate receives a score based on these conditions. One portion of the score describes its response to current input, another describes conjunctions of features, and further terms describe history, phase, and the influence of the prior macrostate. A nonlinear rule converts the score into a gate activation.

The resulting gate vector participates in selecting the next collective state. That collective state, together with the updated history, helps determine which gates become active on the following step.

The exact implementation matters because it creates a loop: local responses contribute to a larger organization, and that larger organization subsequently changes local responsiveness. This is **macrostate causal reentry**. It is a concrete feedback term in the model, rather than a claim that an abstract description causes events independently of its physical realization.

The architecture therefore gives retained history two roles. History influences the present selection, and the present selection changes what history will be carried forward.

### Why trajectories matter more than isolated snapshots

A particular moment of neural activity does not reveal how that state was reached or what its future possibilities are. Two systems may look similar under a coarse present-state measurement while differing in retained variables that affect what they will do next.

The model follows trajectories through a state space. A state space is simply a way of describing each possible configuration as a point, so that continuing activity traces a path.

Under repeated gating, some paths can converge toward similar later conditions. Their earlier differences become less important for the selected outcome. This is **temporal basin compression**: a range of initial trajectories is brought into a narrower set of endpoint regions.

Other paths may separate sharply when a gate changes state. A small difference in timing, context, or retained history can then lead to a different collective regime.

The same network can thus support stable recognition in some circumstances and flexible transitions in others. The relevant organization is a developing route through the network, not merely a code assigned to a single static configuration.

### What the toy simulation reports

The paper implements these principles in a finite computational example with 24 fixed gates. In one reported run, 50,000 sampled signal–context combinations generated 26,683 distinct 24-bit activation patterns. This is a large sampled subset of the formal 16,777,216-pattern space, produced while the local gate architecture remained fixed.

The model also follows trajectories across several updates. After eight steps, four groups of endpoints had reported root-mean-square spread ratios of 0.0089, 0.0504, 0.2834, and 0.2516, relative to their corresponding starting spreads. These numbers describe convergence under the particular statistic and parameterization of the toy model; they do not demonstrate that a biological brain necessarily compresses trajectories by the same amounts.

A separate history comparison held the instantaneous observed-state grid fixed while changing retained-history variables. The reported change in final basin assignment was 59.8% of tested grid locations. The full model states were different because their history carriers differed. This is precisely the intended demonstration: information about prior conditions can change the future through variables that are physically present, even when the selected snapshot appears unchanged.

Another test increased recursive macrostate feedback. Under the reported parameter settings, 86.28% of trajectories at feedback strength ρ = 2.5 remained in the same macrostate through twenty additional updates, and the corresponding proportion reached 100% at ρ = 3.0. This shows how stronger feedback can support longer macrostate residence in the specified construction.

Finally, paired post-perturbation runs compared active macrostate reentry with that feedback term clamped. The reported return fractions were 19.45% and 0.10%, respectively, with final macrostate assignments differing between branches for 53.575% of trajectories. Because the branches shared the same pre-perturbation states and differed in the declared feedback intervention afterward, the comparison illustrates the causal role assigned to that term in the toy model.

These percentages are **reported simulation outcomes**, not newly reproduced results or empirical measurements of consciousness. Independent verification requires the executable specification, fixed parameters, random seeds, labeling procedure, and output data. Their importance is the specificity of the proposed computational tests.

### The Period Lattice as a smaller counting example

Four binary positions provide a compact way to see the difference between detailed arrangements and broader organizational classes. Four sites can occupy sixteen ordered binary configurations. When the arrangements are grouped only by the number of each pole type, five count-based classes remain, with multiplicities 1, 4, 6, 4, and 1.

The five classes preserve a summary of composition while discarding ordering information. If the later dynamics respond to adjacency or orientation, two configurations in the same balance class may have different futures. A coarse description is therefore sufficient only when the distinctions it removes do not affect the target transitions.

The same point matters for neural gating. A total count of active gates may not identify the particular route taken through the network. Their arrangement, timing, and retained context can be indispensable.

### A model of particular conscious contents

The wider account locates the onset of phenomenal interiority at a distinct threshold in the self-maintaining organization of causal flow. Its claim is that ordered interaction, internal reflection, and boundary formation establish a coherent causal interior whose intrinsic side is experience.

The combinatorial gate model concerns a different question: **what gives that continuing interior a particular content?** The proposed answer is the selected history-bearing route through gate activity and larger collective states.

The paper expresses one candidate condition for recursively self-legible organization as:

C_org = T ∧ H ∧ A ∧ K ∧ G

Here T is temporal stabilization, H consequential history, A internal accessibility, K macrostate causal reentry, and G integration across participating processes. The logical conjunction means that all five conditions must hold for the proposed operational criterion.

That formula defines a regime for testing. It is not a proof that any system satisfying five labels is conscious. The underlying measurements must be defined independently, and the sufficiency of the conjunction has to be evaluated against actual systems.

Within a continuing phenomenal interior, the route through the gate repertoire can determine which features become available together, how prior history changes the present interpretation, and which relation is incorporated into what follows.

### Where insight enters

An unresolved question can recruit many partially related representations without making their combined significance recognizable. During insight, a formerly maintained separation gives way, and the contributing relationships become available as a coherent whole.

The gate model offers a candidate account of the route leading to that event: history-sensitive conditions can bring previously dispersed trajectories into a shared collective state. Aleph Harmonic Qualia then proposes that the felt click is the intrinsic character of a specific physical crossing marked by coordinated reorganization and later reuse.

Not every stable macrostate is an insight, and a reduction in the variety of available trajectories is not automatically beneficial. The value of a new organization depends partly on which relationships it makes available and whether the result actually improves later reasoning or recognition.

### Experiments that distinguish the proposal

A neural test can present similar sensory inputs under different learned contexts or with controlled changes in phase and recent history. It can examine whether patterns of reported content correspond to reproducible trajectories through a measured gate space rather than to stimulus identity alone.

A perturbational test can alter the candidate history carrier or feedback process and determine whether the predicted content and subsequent trajectory change together. Comparisons with simpler predictors, including stimulus features, attention, and arousal, are necessary to establish what explanatory value the proposed gating variables add.

The guiding claim is concrete: a finite, continuously organized physical system can generate many particular contents because the same components are reused in different historically conditioned relationships and sequences. The gate repertoire supplies possibilities; the unfolding, history-bearing route selects which possibilities become active within a continuing conscious interior.

---

Full paper on PhilArchive: [The Combinatorial Repertoire of Consciousness](https://philarchive.org/rec/PORTCR-5): *[Context Dependent Gating, Temporal Basin Compression, and Recursive Access](https://philarchive.org/rec/PORTCR-5)*

Before this: [Awareness Where Time Concentrates](https://ahq25.substack.com/p/awareness-where-time-concentrates).

Next: [Stillwater and Death Spirals (the essay)](https://ahq25.substack.com/p/stillwater-and-death-spirals), two pictures of insight.
