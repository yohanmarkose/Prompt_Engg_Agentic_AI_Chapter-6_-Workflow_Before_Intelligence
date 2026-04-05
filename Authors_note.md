# Author's Note
## Chapter 6: Workflow Before Intelligence

---

### The Design Problem I Started With

The chapter's subject — workflow structure in agentic AI systems — is genuinely hard to teach because the core argument is a negative one: the thing students are most likely to optimize for (model intelligence, reasoning capability, prompt sophistication) is not the thing that determines whether a high-stakes system is safe. The design challenge was to make that argument felt before it was stated, not just asserted at the top.

My first output from Bookie led with the Oracle Health framing too quickly. It was technically accurate but read like a product case study rather than an engineering argument. I reprompted with a harder constraint: the student must encounter the failure mode before they encounter the system. That produced the hypothetical overdose scenario in the opening, which works better because the student is already inside the consequence space by the time the three primitives are introduced.

---

### Case Study Decisions

The initial draft contained three case studies presented with false specificity: a dated hospital incident, a named JAMIA publication, and attributed internal Oracle Health documentation. None of these were verifiable. When I caught this, I had two options — replace them with documented cases or reframe them as hypotheticals. I did both, depending on what the case was doing.

The opening overdose scenario is doing rhetorical work: it sets the stakes and makes the structural failure visceral. It does not need to be a specific event to do that job, and representing it as one would have been dishonest. I reframed it as an explicitly hypothetical illustration of a documented failure class, with a sentence pointing the student toward the real literature.

The premature finalization case is doing analytical work: it walks through a specific failure mechanism in enough detail that a student can reason about what the architecture missed. For that purpose, a clearly labeled hypothetical is more useful than a vague gesture at real events, because the student can interrogate the logic rather than deferring to the authority of the citation.

Oracle Health remains named as the chapter's central case, but the framing was revised to be honest about the boundary between the company's public product principles and the illustrative architectural details I constructed around them.

---

### Using Eddi to Revise the Draft

After the initial draft, I ran the chapter through Eddi with two specific instructions: tighten the mechanism section's transitions, and flag any place where a qualitative claim appeared before its quantitative scaffolding. Eddi caught two instances where I had described a workflow pattern as "safer" before the latency arithmetic had been laid out — the conclusion was running ahead of the argument. I moved the arithmetic forward in both cases. Eddi also flagged the Oracle Health attribution language as potentially misleading before I had caught it myself, which accelerated the reframing decision.

---

### Using Figure Architect

I used Figure Architect for the dependency graph section — specifically, the transition from the three independent retrievals (ECG, troponin, medications, allergies, cardiology note) to the visual representation of parallel dispatch and merge. The figure shows five concurrent arrows resolving to a single reasoning node, with the data completeness gate sitting between the merge and the reasoning layer. Without the figure, that section asked students to hold a five-node graph in working memory while reading prose about it. With it, the prose explains what the student is already seeing. I also requested a figure for the sequential dependency chain showing the compliance lock-and-key structure, which anchors the contrast between sequential and parallel before the student has to hold both in mind simultaneously.

---

### Self-Assessment

The chapter is strongest in its mechanism section and its closing argument. The three-primitive framework is built with enough quantitative specificity — the latency arithmetic, the dependency mapping discipline, the data completeness gate logic — that a student can actually use it, not just name it. The closing argument about the permanence of human approval gates is the chapter's most important claim and the one most likely to be challenged; I think it holds, but it would benefit from a counterargument section in a future revision.

The learning outcomes added in the Chapter Foundation section are the element I am most confident about. Each one maps to a specific section of the chapter, requires a specific cognitive operation, and points toward a specific failure mode the chapter is designed to prevent. Outcome 5 in particular — the critique of human gates as temporary scaffolding — ensures that the chapter's closing argument is not merely read but contested, which is where the real learning happens.
