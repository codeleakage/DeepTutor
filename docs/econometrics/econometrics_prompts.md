# Econometrics Prompt Templates for DeepTutor

These prompt templates are designed for repeated use in DeepTutor while studying econometrics.

## General study template

```text
I am studying econometrics.
Topic: [TOPIC]

Please answer in this order:
1. Core concept
2. Required assumptions
3. Intuition
4. Mathematical explanation
5. Small example
6. Common mistakes
7. Three check questions
```

---

## OLS concept template

```text
I am studying introductory econometrics.
Explain OLS in the following order:
1. Objective of OLS
2. Model setup
3. Why least squares is used
4. Intuition of the coefficient
5. Main assumptions
6. What goes wrong when assumptions fail
7. A very small numerical example
```

## OLS derivation template

```text
Derive the OLS estimator step by step.
Requirements:
- do not skip algebra steps
- explain what each symbol means
- explain the economic meaning of the coefficient
- end with a short summary of the derivation logic
```

## OLS assumptions review template

```text
I want to review OLS assumptions.
For each assumption:
1. State it formally
2. Explain it intuitively
3. Explain why it matters
4. Give an example of violation
5. Explain what happens to estimation or inference
```

---

## Omitted variable bias template

```text
Explain omitted variable bias in the following order:
1. Definition
2. Why it occurs
3. Bias formula or sign logic
4. How the bias direction is determined
5. Economic example
6. Why this creates a problem for causal interpretation
7. Three review questions
```

## Heteroskedasticity template

```text
Explain heteroskedasticity in the following order:
1. Formal definition
2. Intuition
3. Why OLS coefficients can still be unbiased
4. Why standard inference becomes problematic
5. What robust standard errors do
6. A small example
7. Common student misunderstandings
```

## Autocorrelation template

```text
Explain autocorrelation for econometrics students.
Please include:
1. Definition
2. Intuition
3. Difference from heteroskedasticity
4. Why it is especially important in time series
5. Effect on inference
6. Typical remedies
```

---

## IV template

```text
Explain instrumental variables in the following order:
1. Why OLS fails in this setting
2. What an instrument is
3. Relevance condition
4. Exogeneity condition
5. Intuition for two-stage least squares
6. Example from economics
7. Common mistakes in interpretation
```

## Fixed effects template

```text
Explain fixed effects in the following order:
1. Model intuition
2. What fixed effects remove
3. Why this helps with omitted variables
4. Limits of fixed effects
5. Difference from pooled OLS
6. Difference from random effects
7. Small panel-data example
```

## Difference-in-differences template

```text
Explain difference-in-differences for an econometrics student.
Include:
1. Research setup
2. Estimand intuition
3. Parallel trends assumption
4. Common threats to validity
5. Event-study connection
6. Example from policy analysis
```

---

## Paper reading template

```text
I am reading an econometrics or empirical economics paper.
Please analyze it in this order:
1. Research question
2. Outcome variable
3. Key explanatory variable
4. Identification strategy
5. Main assumptions
6. Possible threats to validity
7. Robustness checks I should look for
8. How cautious I should be about causal claims
```

## Regression table interpretation template

```text
Help me read a regression table.
For each column:
1. What changes relative to the previous column
2. What the key coefficient means
3. Whether the sign and magnitude make sense
4. Whether the result looks causal or only associational
5. What extra information I should check
```

---

## Quiz generation template

```text
Create a quiz on [TOPIC].
Requirements:
- number of questions: [N]
- difficulty: [easy / medium / hard]
- include both concept and interpretation questions
- do not show answers first
- after I answer, grade me and explain each mistake
```

## Weak-point drill template

```text
My weak topics are: [TOPICS].
Create a focused practice set that targets only those weak points.
For each question:
- test a different misunderstanding
- keep the wording clear
- after grading, summarize the recurring pattern in my mistakes
```

---

## Research comparison template

```text
Compare [METHOD A] and [METHOD B] in applied econometrics.
Please include:
1. When each method is used
2. Main identifying assumptions
3. Strengths
4. Weaknesses
5. Typical mistakes by beginners
6. Which kinds of research questions each method fits best
```

## Study summary template

```text
Summarize what I studied today.
Please organize the summary into:
1. Concepts I understood well
2. Concepts that are still weak
3. Formulas I should review
4. One or two likely exam traps
5. What I should study next
```

## Tutor behavior template

```text
Act as a rigorous econometrics tutor.
My preferences:
- explain with formula + intuition + example
- be precise about assumptions
- clearly separate association from causality
- do not jump to the final answer when I ask derivation questions
- ask me one checking question before closing the explanation
```

---

## Suggested usage

A strong default sequence is:

1. Start with the general study template
2. Move to a method-specific template
3. Use the quiz template after each topic
4. End with the study summary template

This makes DeepTutor behave more like a structured tutor and less like a generic assistant.
