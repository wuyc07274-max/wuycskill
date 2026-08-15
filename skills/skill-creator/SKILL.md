---
name: "skill-creator"
description: "Create new skills, modify/improve existing ones, and measure skill performance"
---

# Skill Creator

A skill for creating new skills and iteratively improving them.

## Process
1. Decide what the skill should do and how
2. Write a draft of the skill
3. Create test prompts and run claude-with-access-to-the-skill on them
4. Evaluate results qualitatively and quantitatively
5. Rewrite based on feedback
6. Repeat until satisfied
7. Expand test set and test at larger scale

## Key Features
- Create skills from scratch
- Modify and improve existing skills
- Run evals to test skills
- Benchmark skill performance with variance analysis
- Optimize description for better triggering accuracy

## Workflow
Uses `eval-viewer/generate_review.py` to show results, runs background evaluations while drafting quantitative evals.
