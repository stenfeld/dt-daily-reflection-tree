# DT Daily Reflection Tree

This repository contains my submission for the DT Fellowship assignment.

## Included Files
- `tree/reflection-tree.json` — main deterministic tree data
- `tree/tree-diagram.md` — visual branching diagram using Mermaid
- `write-up.md` — design rationale and psychological grounding
- `transcripts/persona-1-transcript.md` — sample path for a more victim/entitled/self-focused persona
- `transcripts/persona-2-transcript.md` — sample path for a more agentic/contribution-oriented/wider-concern persona

## Design Summary
The reflection system is designed as a deterministic, fixed-choice end-of-day tool. It moves through three axes in sequence:

1. Locus: Victim vs Victor  
2. Orientation: Contribution vs Entitlement  
3. Radius: Self-centric vs Wider Concern

Each answer adds a signal. Decision nodes compare tallies and route the employee to the appropriate reflection. No free text and no runtime LLM are used.

## How To Read The Tree
- Question nodes present fixed options
- Each option adds one or more signals
- Decision nodes compare totals and choose a known next step
- Reflection nodes provide reframing without moralizing
- Bridge nodes connect one axis to the next
- Summary and end nodes close the experience

## Notes
This submission focuses on Part A strongly. The structure is readable as data and can later be loaded by a simple CLI or web-based agent.
