# DeepTutor for Econometrics Study

This document explains how to use DeepTutor as a personalized econometrics study system rather than as a general chat app.

## Goal

Use DeepTutor to build a repeatable workflow for:

- concept learning
- derivation and proof practice
- quiz-based reinforcement
- paper reading and identification analysis
- notebook-based review
- long-term weak-point tracking

## Why DeepTutor fits econometrics study

DeepTutor already provides the pieces needed for a strong study loop:

- **Chat** for concept explanations and quick Q&A
- **Deep Solve** for derivations, proofs, and step-by-step reasoning
- **Quiz Generation** for practice and review
- **Deep Research** for literature and methodology comparison
- **Guided Learning** for structured weekly learning plans
- **Knowledge Base** for grounding answers in your own notes and textbooks
- **Notebook + Memory** for cumulative review and personalization
- **TutorBot** for persistent role-based tutors

The key idea is simple: turn DeepTutor into an **econometrics-specific personal tutor system**.

## Recommended project structure

```text
project/
├─ study_plan/
│  └─ econometrics_study_plan.md
├─ materials/
│  ├─ textbooks/
│  ├─ lecture_notes/
│  ├─ papers/
│  └─ formulas/
├─ prompts/
│  └─ econometrics_prompts.md
├─ weekly_notes/
│  ├─ week01.md
│  ├─ week02.md
│  └─ ...
└─ errors_and_reviews/
   └─ weak_points.md
```

### How each folder maps to DeepTutor

- `materials/` -> upload into a knowledge base
- `study_plan/` -> use as the skeleton for Guided Learning
- `prompts/` -> keep reusable prompting templates
- `weekly_notes/` -> save outputs into notebooks
- `errors_and_reviews/` -> track recurring mistakes and weak areas

## Setup strategy

### 1. Build an econometrics knowledge base

Recommended knowledge base name:

```bash
deeptutor kb create econometrics-kb --doc materials/textbooks/main_textbook.pdf
deeptutor kb add econometrics-kb --docs-dir ./materials/
deeptutor kb set-default econometrics-kb
```

Suggested contents:

- textbook chapters or summaries
- lecture notes
- theorem and formula summaries
- worked solutions
- paper summaries
- personal review notes

Do not treat the knowledge base as storage only. It should become the grounding source for explanations, quizzes, and research outputs.

### 2. Use Guided Learning as the main learning path

Use the study plan markdown file as the base document for a guided path such as:

1. Probability and statistics review
2. OLS basics
3. OLS assumptions and violations
4. Heteroskedasticity and autocorrelation
5. Endogeneity and omitted variable bias
6. IV
7. Panel data and fixed effects
8. Difference-in-differences
9. Time series basics
10. Paper reading and empirical interpretation

A good DeepTutor workflow is:

- let Guided Learning split the topic into learning steps
- study one step at a time
- ask questions next to each step
- save the best explanations to a notebook

## Role-based use of capabilities

### Chat

Use Chat for:

- concept explanations
- notation clarification
- regression output interpretation
- quick comparison of methods

Good examples:

- Explain the intuition of OLS under conditional mean zero.
- What does omitted variable bias mean in plain language?
- Compare fixed effects and random effects intuitively.

### Deep Solve

Use Deep Solve for:

- derivations
- proofs
- difficult homework-style reasoning
- step-by-step mathematical interpretation

Good examples:

- Derive the OLS estimator in matrix form.
- Show why heteroskedasticity does not bias OLS coefficients but affects inference.
- Derive the omitted variable bias formula and interpret the sign.

### Quiz Generation

Use Quiz Generation for:

- weekly review
- low-stakes recall checks
- exam-style concept reinforcement
- targeted weak-point drills

Good examples:

- Generate 10 questions on OLS assumptions and violations.
- Give me 5 medium-difficulty questions on IV and fixed effects.
- Create a mixed quiz from chapters 1 to 4, but hide the answers first.

### Deep Research

Use Deep Research for:

- comparing methods
- literature overviews
- empirical strategy analysis
- identification critique

Good examples:

- Compare IV, FE, and DiD for causal inference in economics.
- Summarize the key assumptions behind DiD and how researchers test them.
- Review how panel models are used in applied labor economics.

## Recommended TutorBot setup

Create multiple bots with separate responsibilities rather than relying on one general tutor.

### 1. Concept tutor

Purpose:

- explain definitions clearly
- connect formulas and intuition
- summarize assumptions precisely

Example:

```bash
deeptutor bot create econ-concept-tutor --persona "Rigorous econometrics tutor who explains formulas, intuition, and assumptions together."
```

### 2. Problem-solving tutor

Purpose:

- guide derivations
- ask leading questions
- avoid giving answers too early

Example:

```bash
deeptutor bot create econ-problem-tutor --persona "Socratic econometrics tutor who gives hints before revealing full solutions."
```

### 3. Research tutor

Purpose:

- analyze empirical papers
- inspect identification strategies
- point out robustness issues

Example:

```bash
deeptutor bot create econ-research-tutor --persona "Research-oriented econometrics mentor focused on identification, assumptions, and robustness."
```

## Suggested weekly workflow

### Monday

Read the main concept and use Chat for understanding.

```bash
deeptutor run chat "Explain OLS assumptions clearly and intuitively." -t rag --kb econometrics-kb
```

### Tuesday

Use Deep Solve for derivation or proof work.

```bash
deeptutor run deep_solve "Derive the OLS estimator in matrix form and explain each step." -t reason
```

### Wednesday

Generate a quiz and solve it yourself.

```bash
deeptutor run deep_question "OLS assumptions, omitted variable bias, and heteroskedasticity" --config num_questions=5
```

### Thursday

Use Deep Research to connect the topic to applied work.

```bash
deeptutor run deep_research "How are fixed effects used in applied econometrics papers?"
```

### Friday

Review the week and save outputs.

- save strong explanations into a notebook
- save wrong answers into a weak-point note
- summarize what still feels unclear

## Notebook strategy

Recommended notebooks:

- `econometrics-concepts`
- `econometrics-derivations`
- `econometrics-paper-notes`
- `econometrics-mistakes`

This separation makes review much easier later.

## Memory strategy

DeepTutor memory becomes more useful if your prompts are consistent.

Examples of useful persistent information:

- your current study stage
- whether you prefer hints before answers
- whether you want formula-first or intuition-first explanations
- which topics are weakest right now

Suggested recurring note:

- I want rigorous but readable explanations.
- I prefer formula + intuition + example.
- Do not jump to the final answer in derivation problems.
- Track weak points in IV, FE, and inference.

## What not to do

Avoid these habits:

- using Chat only and ignoring Quiz/Deep Solve
- asking for final answers immediately
- storing materials without building a usable knowledge base
- mixing all notes into one notebook
- treating statistically significant coefficients as automatically causal

## Minimal high-value workflow

If you want the simplest setup that still works well:

1. Create `econometrics-kb`
2. Upload your notes and textbook summaries
3. Use Guided Learning from the study plan
4. Use Chat for explanation
5. Use Deep Solve for derivations
6. Use Quiz Generation every week
7. Save mistakes in a dedicated notebook

## One-line summary

Use DeepTutor as a **role-based, notebook-backed, knowledge-grounded econometrics tutor system**: explain, derive, quiz, research, review, and improve in one continuous workflow.
