# Instruction Mode, Note-Taking Method, and Quiz Performance

A 2×3 completely randomized factorial experiment examining how instruction mode and note-taking method affect quiz performance.

**Course:** STAT 5604, Experiments: Knowledge by Design — Temple University
**Team:** Team Fukuro

## Overview

This project investigates whether students perform differently on a short quiz depending on (1) how instructional content is delivered and (2) how they take notes while learning it. Seventy-two participants were randomly assigned to one of six treatment combinations, watched the same instructional video on recognizing AI-related scams, and completed an identical 10-question quiz.

**Research question:** How do instruction mode and note-taking method affect students' quiz performance, and does the effect of note-taking method depend on whether instruction is delivered virtually or in person?

## Experimental Design

- **Factor A — Instruction Mode:** Virtual, In-person
- **Factor B — Note-Taking Method:** Handwritten, Laptop, No notes
- **Design:** Completely randomized 2×3 factorial, 12 participants per treatment combination (n = 72 total)
- **Response variable:** Quiz score (0–10, total correct answers)

## Methods

- Two-way ANOVA with interaction, fit in R (`aov()`)
- Tukey's HSD for pairwise comparisons of note-taking method
- Interaction plot to visually assess whether the effect of note-taking method depended on instruction mode

## Key Findings

- **Note-taking method** had a statistically significant effect on quiz scores (F(2, 66) = 6.72, p = 0.0022). Students who took handwritten notes scored significantly higher than students who took no notes (Tukey HSD, adjusted p = 0.0015).
- **Instruction mode** had no significant effect on quiz scores (F(1, 66) = 0.005, p = 0.94).
- **Interaction** between instruction mode and note-taking method was not statistically significant (F(2, 66) = 1.04, p = 0.36).

## Repository Contents

| File | Description |
|---|---|
| `*.Rmd` | R Markdown source: full analysis code and write-up |
| `*.html` | Knitted HTML output of the analysis |
| `*_presentation.*` | Project presentation slides |
| `quiz_data.csv` | Raw dataset (student ID, instruction mode, note-taking method, quiz score) |

## Tools

R, tidyverse, mosaic, ggplot2, aov(), TukeyHSD()
