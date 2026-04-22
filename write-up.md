# Design Write-Up

## 1. Design Goal
This reflection tool is designed as a deterministic end-of-day reflection system. The goal is to guide an employee through a structured conversation using fixed options, predictable branching, and reflection prompts without relying on any LLM at runtime.

## 2. Why I Chose These Questions
I designed the questions to feel realistic for a tired employee at the end of a workday. Instead of asking direct moral questions, I used believable workplace choices that indirectly surface deeper patterns in how the employee interprets the day.

The questions are intentionally short, clear, and fixed-choice. This makes the tree auditable and ensures that every answer leads to a known next node.

## 3. Tree Structure and Branching Logic
The tree is organized across three psychological axes in sequence:

1. Locus: Victim vs Victor  
2. Orientation: Contribution vs Entitlement  
3. Radius: Self-centric vs Wider Concern

Each axis contains three question nodes. Each option adds a signal to one side of that axis. After the three questions, a decision node compares the tallies and routes the user to a reflection node. A bridge node then transitions the employee into the next axis.

This design keeps the flow conversational rather than turning the assignment into three separate quizzes.

## 4. Trade-offs I Made
I preferred clarity and determinism over complexity. Instead of creating too many nuanced edge cases, I focused on making the structure readable, consistent, and easy to inspect as data.

I also chose JSON because it is clean, readable, and easy to load later into a simple CLI or web-based agent.

## 5. Psychological Sources Used
The design was informed by the following ideas:

- Julian Rotter’s Locus of Control
- Carol Dweck’s Growth Mindset
- Organizational Citizenship Behavior
- Psychological Entitlement research
- Self-transcendence and perspective-taking frameworks

These ideas helped shape the three axes and the wording of the questions and reflections.

## 6. Tone and Design Principles
I tried to keep the tone supportive, honest, and non-moralizing. The reflection should increase self-awareness, not shame the employee. The goal is not to judge the user, but to help them notice where their attention and interpretation went during the day.

## 7. What I Would Improve With More Time
With more time, I would improve the tree in four ways:

- Add more nuanced middle states between both ends of each axis
- Add richer summary templates using safe interpolation
- Build and test a runnable CLI agent for Part B
- Create more transcript-based testing across multiple employee personas
