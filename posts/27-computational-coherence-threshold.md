# A Minimal Computational Test of the Coherence Threshold

- **Author:** Quinn Porter
- **Audience:** everyone (free, public; intended for synchronization)
- **Mirror status:** Existing Substack URL not recorded; check by title before creating a new post.

---

The transition from a proposed organizing principle to an explicit computational model is important because a model forces every operation to be specified. A statement that local activity can preserve its organization must become an update rule. A claim that restoration competes with disruption must identify what each operation changes. A threshold requires a measurable outcome that can vary across the chosen parameter range.

[Deriving the Coherence Threshold](https://philarchive.org/rec/PORDTC) uses a finite lattice of interacting binary sites to investigate these relationships. The purpose of the model is to show how local updates can favor particular junction patterns and how repeated updates can change the organization visible across a field.

The underlying computation is a toy dynamical construction. Its qualitative pictures should not be mistaken for a measured universal Porter Ratio threshold or for evidence of phenomenal experience.

### The states available at one junction

The model uses a square grid whose sites can occupy either of two states, labeled p and d. A junction is defined by four neighboring sites. Each site has two possibilities, so a junction has

**2⁴ = 16 ordered binary states.**

Those states can be grouped by the number of p sites. The five possible counts are 0, 1, 2, 3, and 4, with respective multiplicities 1, 4, 6, 4, and 1.

These numbers are exact combinatorics. They do not depend on the simulation's randomness or on any claim about consciousness.

The grouping discards arrangement information. Two p sites on adjacent corners and two p sites on diagonally opposite corners belong to the same count-based class even though their geometries differ. A count-based model can therefore measure a simple property without preserving every relational distinction in the full Period Lattice.

### What the computer actually does

The source paper includes a short Python implementation built around a randomly initialized 40 × 40 grid. One operation flips a selected site, changing p to d or d to p.

An environmental update draws a random number of flips from a Poisson distribution whose mean is proportional to a specified disruption parameter and the total number of sites. This injects stochastic changes into the field.

The operation called restoration repeatedly chooses a four-site junction. It counts how many of the four sites are p, selects a flip probability based on that count, and sometimes flips one randomly selected site.

The rule favors updates in more imbalanced junctions: configurations with zero or four p sites are assigned a larger flip probability than those with two p sites. At an extreme junction, flipping any one site decreases the imbalance. At a one-p or three-p junction, a random flip decreases imbalance in three of the four possible site choices but increases it in the remaining choice. At a balanced junction, any flip creates an imbalance. Thus the update has a directional bias rather than a guarantee of improvement, and overlapping junctions can complicate the field-wide result. The term **restoration** refers to the update rule's intended aggregate bias, not a guarantee that each flip corrects a disturbance. A restoration rate must be measured from the actual change in the declared organizational observable, because the number of attempted corrections alone does not establish how much organization was restored.

Neighboring junctions overlap. Flipping one site can therefore change several local counts at once. This overlap supplies a concrete coupling mechanism through which local updates can influence patterns elsewhere in the grid.

### The measured coherence variable

The implementation's stated coherence function measures the fraction of four-site junctions containing exactly two p sites and two d sites.

**C = N_(2p2d) / N_junctions**

This variable is well defined for the chosen grid. It reports how much of the observed field occupies the selected count-based balance class.

The statistic has a calculable random reference. If the four site states are independent and each has probability one-half of being p, exactly six of the sixteen equally likely assignments contain two p and two d states. The expected balanced-junction fraction is therefore **6/16 = 0.375**. More generally, if independent sites have p probability q, the expected fraction is **6q²(1 − q)²**. That baseline changes with the overall prevalence of p states, even without spatial organization. A meaningful test should compare the observed C against the appropriate occupancy-matched reference and report uncertainty and spatial correlations, rather than interpreting C alone as a universal coherence score.

The measure does not identify which exact arrangements occur inside that class. It does not measure all forms of spatial correlation, does not separately quantify historical influence, and does not establish that the field has formed an integrated boundary. For example, an alternating checkerboard and many differently arranged fields can attain a high fraction of balanced junctions without having equivalent routes of influence or the same response to a disturbance.

In particular, a rise in C demonstrates greater prevalence of the chosen local pattern. Any stronger description, such as a coherent wave traveling across the field, requires additional measurements of spatial propagation over successive times, not merely a final grid image.

### What the low- and high-restoration examples compare

The source code includes two illustrative conditions. Both begin from a randomized grid with a fixed seed and introduce a forced flip followed by an environmental update. The conditions then differ markedly in the number of attempted restoration updates.

The lower-restoration example applies five restoration attempts. The stronger condition applies twenty rounds of fifty attempts, or one thousand attempts in total. This is a change in the number of update opportunities under the specified code.

The source paper labels its plotted examples as low R and high R, including the numbers 0.5 and 5. Those labels should **not** be treated as independently measured values of λ_self / λ_env. The code supplies a disruption parameter and a count of restoration attempts, but does not estimate the two effective rates for the same organizational observable and interval and then calculate R from those estimates.

The defensible reading of the example is therefore a comparison of **low and high restoration-update effort under a particular stochastic model**. Assigning actual Porter Ratios requires a separate operational rate-calibration procedure.

This distinction strengthens the research design by identifying the next measurement that the toy model needs.

### From a restoration bias to a genuine threshold test

A prospective computational experiment would define the organizational variable to be maintained and measure both the rate at which the restoration rule changes that variable and the rate at which disruption changes the same variable.

Multiple randomized runs across a range of fixed parameters could then estimate those rates and their variability. The ratio would be calculated only after the two terms have a common measurement basis.

The model would also need an outcome defined independently of R. For example, sustained spatial connectivity, recovery after standardized perturbation, reproducible domain formation, or measured propagation of correlations could define a transition of interest.

The next question would be whether a particular R★ predicts that transition in runs not used to estimate the threshold. Connectivity, restoration-attempt count, the difference between the rates, and the two rates separately should be tested as alternative predictors.

Without this calibration, the model shows that update rules can generate different-looking or differently balanced fields; it does not yet derive a specific boundary-forming threshold from the Porter Ratio.

### History in a finite lattice

A state of the lattice at one time depends on earlier updates because those updates changed the current arrangement. That gives the simulation an ordinary physical and mathematical history.

A stronger claim of **active inheritance** requires identifying the retained organization that changes how later interactions proceed. In the given implementation, local junction counts influence the probability of subsequent flips. The current pattern therefore conditions the update process that will act on it.

This history dependence is implemented through the present grid. No earlier state exerts an influence outside the current model variables; the current arrangement is the carrier of earlier changes.

An experiment can compare matched coarse measurements under different detailed grid configurations. If two fields have the same fraction of balanced junctions but different arrangements, their later evolution may differ because the update rule responds to local patterns. The complete current grids are different, even though the reported scalar coherence scores match.

This is a useful illustration of why a coarse variable can omit consequential structure.

### The relation to the Period Lattice

The Period Lattice starts with an exact space of possible local configurations and their relations. The computational model adds a rule that moves among those configurations over successive steps.

The two contributions should remain distinct. State counting determines what is combinatorially possible at a junction. The update rule determines which configurations become more common, which spatial relationships persist, and whether changes propagate through the field.

The particular balance-based restoration rule is only one possible dynamics over the finite state space. An alternative rule that preserves orientation, favors a different count class, or couples junctions nonlocally could produce very different results.

This is a strength of the modeling approach: the dynamics can be varied while holding the underlying combinatorics fixed, allowing the effect of each chosen physical assumption to be isolated.

### Where a causal interior would enter

The broader theory proposes that ordered causal flow, internal reflection, recirculation, and sustained selective interaction can generate a self-maintaining causal boundary. It associates the formation of that coherent interior with a system-specific threshold R★ and proposes phenomenal experience as its intrinsic aspect.

A two-dimensional grid with biased local flips does not automatically possess this full architecture. Local restoration can occur without a dynamically individuated inside and outside. More structured boundary rules, exchange conditions, retained carriers, and feedback among levels would be needed to examine the proposed formation mechanism directly.

Even if those features were implemented and a sharp organizational transition were measured, an additional identity hypothesis would still connect the external physical transition to phenomenal experience. Simulation of one measurable organizing process is not a direct reading of the intrinsic character of that process.

The model is therefore most useful as an early component of the causal argument, not as its final demonstration.

### A reproducible development path

The source paper supplies example Python code, including random initialization, environmental flips, restoration attempts, and the coherence statistic. A rigorous follow-up would report all parameters, seeds, iteration counts, measurements over time, and outcomes across many repeated runs rather than relying on selected images.

The critical additions are straightforward: calculate the actual effective restoration and disruption rates, report uncertainty, define a spatially meaningful boundary outcome, measure propagation rather than infer it from a snapshot, and compare the proposed ratio against simpler quantities.

That expanded protocol could show whether a genuine organizational transition occurs under the chosen rules, whether a reproducible R★ helps locate it, and how changing local coupling alters its appearance.

The finite lattice is valuable because every assumption is inspectable and every update can be modified. Its current result is a concrete demonstration that local probabilistic rules can favor some organizations over others. The proposed link from that behavior to a measured self-maintaining boundary remains a precise next question for computation and experiment.

---

Full paper on PhilArchive: [Deriving the Coherence Threshold](https://philarchive.org/rec/PORDTC)
