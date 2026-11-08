## Stage 1 — Acquisition (CM3: acquisition patterns, provenance, access rules)
**Reflect:** `rp.read()` (the "obvious" one-liner version of this check) silently
returns "disallow everything" on a network with a proxy in front of it — with no
error, no warning, nothing that looks broken. `rp.parse()` (used above) doesn't have
this problem. In your own words: why is a pipeline stage that fails *silently* worse
than one that crashes loudly, for something whose whole job is "respect the rules
before acting"? Tie your answer to CM3's provenance argument.

It's important to keep track of your source and make sure it is a legal source. Having a silent fail means that you cannot backtrack to the origin of the information but nothing in the pipeline notifies this problem.

**Reflect:** France Travail's API (used in TP1's main pipeline) is official
government open data, explicitly licensed for reuse. This jobspy-derived sample is
not. In your own words, what's the actual difference in risk between the two? Would
your answer change if this repo were private instead of public — and if so, why does
public/private matter here at all?

A dataset that is explicitly licensed for reuse is safe to use in a public repo as long as I follow the licence's conditions. The jobspy sample has already been scraped. It is probably illegal to redistribute it so a private repo is advised.

## Stage 2 — Structuring (CM5: agentic AI earns its place, or it doesn't)
**Reflect, before you run anything:** CM5 argues agentic AI belongs at specific
pipeline stages, not everywhere. This TD extracts skills with an LLM, but nothing in
this course ever uses an LLM to decide, say, which application you actually sent or
what your real skill level is. Using CM5's own distinction (not just "because it's
convenient"), explain in your own words *why* free-text-to-structured-list is a good
fit for an LLM and a plain record of your own actions is not.

An LLM is good at summing up things, it can pick up the most important things in a text, the most important word in a phrase, faster and probably more accurately than a human. A plain record of my own actions is imprecise, long to read, it has mistakes in it. 
The "silent failure" of an LLM here is just the same as a silent failure from human error.

## Stage 3 — Data quality (checking what the model actually gave you)
**Reflect, before reading further:** you just ran the exact same prompt, the exact
same model, across several different postings. Even when the model correctly
identifies the right skills, what specific *formatting* inconsistency would you
expect across independent calls — the same real skill written two different ways?
Write your prediction down first.

I would expect synonyms of the words in previous iterations, maybe a different order in the list, maybe 1 or 2 different words.

