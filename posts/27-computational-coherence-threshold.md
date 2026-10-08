# A Minimal Computational Test of the Coherence Threshold

A framework built around restoration, disruption, and threshold formation should be implementable as an explicit dynamical system. [Deriving the Coherence Threshold](https://philarchive.org/rec/PORDTC) provides a small reproducible model for that purpose.

The model is intentionally minimal. It does not reproduce a living organism or establish that the Porter Ratio is a universal law. Its job is narrower and more useful: to show that the proposed competition between restoration and disruption can be written as explicit rules, run repeatedly, and produce distinct organizational regimes that can be measured.

### From a static state space to a dynamical field

The simulation uses a two-dimensional field of binary states. Local groups of four sites form junctions with the same five balance classes that appear in the Period Lattice. Four binary positions give sixteen ordered microstates, and grouping them by pole count gives five balance classes with multiplicities

1, 4, 6, 4, 1

That is the static combinatorial part. The computational model adds dynamics.

Environmental disruption changes local states stochastically. Internal restoration applies local rules that tend to rebuild the declared organization. Their relative effective rates are summarized by

R = λ_self / λ_env

The model then tracks what happens to local and field-scale organization as these processes act repeatedly.

### What changes as R changes

Under the stated toy update rules, disruption-dominated runs can erase or scatter retained structure faster than the restoration rule rebuilds it. That behavior is a property to measure in the constructed model, not a universal consequence of R < 1: different interaction rules can instead spread perturbations through a field.

Under the chosen model rules, increasing restoration relative to disruption can allow local corrections to persist and overlap. Correlations may then extend farther through the field, and carried organization may exert more influence on later states. The ratio is one control coordinate; connectivity, update order, interaction geometry, and retention rules also help determine the result.

The important result is not that one particular numerical value of R has been proven to be a universal threshold. The result is that a change in the balance between restoration and disruption can generate a reproducible transition in the organization of a controlled system.

That gives the threshold idea a concrete computational meaning.

### Why this matters

The model establishes three things.

First, the restoration-versus-disruption relation can be implemented with explicit update rules and measurable quantities rather than remaining only a verbal analogy.

Second, repeated local interactions can generate a change from a disruption-dominated regime to a more extended, restoration-dominated organization.

Third, the model is specified as a candidate for reproducible testing. Independent reproduction requires access to the complete update rules, lattice size, initialization, random seeds, parameter choices, coherence measure, and implementation or equivalent executable specification. A reader should be able to alter those assumptions and test whether the reported transition survives. The prose description alone is not a completed independent replication.

That last point is especially important. A useful toy model should expose the framework to failure, not insulate it from criticism.

### What the model does not establish

A computational transition is not evidence by itself that biological systems cross the same threshold, and it does not establish phenomenality.

The model is presented as a constructive example of the dynamical architecture: explicit restoration and disruption rules can produce different organizational regimes under suitable coupling and update assumptions. The simulation result depends on those declared rules; a mathematical statement about all possible restoration/disruption systems does not follow. Independent execution is needed to verify the particular run, and empirical support requires separate measurements in physical and biological systems.

Likewise, the phenomenal claim remains a distinct identity claim. In the wider framework, R★ marks the empirical boundary-forming transition for a declared system, and boundary formation is identified with interior formation. Phenomenal experience is proposed as the intrinsic side of that formed interior. A toy simulation can help define and detect the boundary transition. It cannot by itself verify the intrinsic side of that event.

This separation keeps the computational result honest.

### Relation to the Period Lattice

The Period Lattice describes organizational possibility before the dynamics are added. It distinguishes exact local arrangement from balance class, composition from relational order, and local state from shared-boundary organization.

The simulation takes that local combinatorial structure and asks what happens when restoration and disruption repeatedly move the field through those possibilities.

This creates a useful bridge. The lattice asks, **what states and relations are available?** The dynamical model asks, **which of those organizations persist, spread, or disappear when restoration competes with disruption?**

The two therefore play different roles. The Period Lattice supplies a state space and relational geometry. The computational model supplies an update process.

### Relation to consequential history

The model also clarifies why persistence and history belong together. When restoration is weak, previous organization is rapidly overwritten and has little opportunity to constrain later states. As restoration strengthens, more of the earlier arrangement survives long enough to affect subsequent transitions.

That is the minimal computational form of consequential history: the past remains active because some consequence of earlier organization still participates in producing what happens next.

In a biological experiment, a stronger test would match selected observable present variables while manipulating or measuring additional present carriers of retained history, then ask whether later trajectories diverge. The complete physical state is not held identical when a history carrier is changed. The toy model prepares that causal question without pretending to answer it for living systems.

### The larger picture

The computational model belongs near the bottom of the evidential ladder, not at the top. It shows implementability. The bacterial protocol supplies an experimental route. Cross-system measurement would determine whether the Porter Ratio predicts natural transitions better than simpler alternatives.

The conceptual sequence remains the same: restoration allows organization to persist; persistence allows consequential history to remain active; a system-specific threshold may mark the formation of a coherent causal boundary; boundary formation is the proposed onset of interiority; phenomenal experience is the intrinsic side of that event; and recursive availability describes deeper self-legibility within the formed interior.

The value of the model is that the first part of that sequence can be run, measured, modified, and challenged directly.

---

Full paper on PhilArchive: [Deriving the Coherence Threshold](https://philarchive.org/rec/PORDTC)
