<div align="center">

# Week 05: Symbol Grounding and Meaning

**Philosophy of Artificial Intelligence (11118BLG003)**  
Prof. Dr. Utku Kose, Süleyman Demirel University

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/utkukose/philosophy-of-ai-NB-lecture/blob/main/weeks/week-05/NB05_symbol_grounding.ipynb) [![Interactive lab](https://img.shields.io/badge/interactive%20lab-open-1D5B78)](https://utkukose.github.io/philosophy-of-ai-NB-lecture/weeks/week-05/lab.html) [![Lecture notes](https://img.shields.io/badge/lecture%20notes-PDF-566A73)](Week05_Lecture_Notes.pdf) [![Course home](https://img.shields.io/badge/course-home-B97813)](../../README.md)

</div>

## Overview

How can the symbols of a system mean anything to the system itself? This week examines the symbol grounding problem and the distributional view of meaning that underlies language models. It then turns to the argument that form alone cannot yield meaning, and to replies that locate meaning in conceptual roles or learned relations [1, 2, 3].

**Estimated study time:** 6 to 8 hours.

## Learning outcomes

By the end of the week, students are expected to state the symbol grounding problem and Harnad's proposed solution. They should be able to compute distributional word representations and interpret their similarities. They should also be able to reconstruct the octopus argument of Bender and Koller and to evaluate replies based on conceptual roles and vector grounding.

## Study path

| Step | Activity | Suggested time |
|---|---|---|
| 1 | Read the lecture below or the [PDF version](Week05_Lecture_Notes.pdf) | 90 minutes |
| 2 | Explore the [interactive lab](https://utkukose.github.io/philosophy-of-ai-NB-lecture/weeks/week-05/lab.html) | 45 minutes |
| 3 | Work through the [Colab notebook](https://colab.research.google.com/github/utkukose/philosophy-of-ai-NB-lecture/blob/main/weeks/week-05/NB05_symbol_grounding.ipynb) and its exercises | 2 to 3 hours |
| 4 | Take the self-assessment in the interactive lab (tab: Check yourself) | 20 minutes |
| 5 | Answer the reflection prompts in the interactive lab, export the learning log and complete the weekly task | 60 minutes |

## Week at a glance

```mermaid
flowchart LR
  S["Symbols"] --> D["Dictionary-go-round: symbols defined by symbols"]
  D --> G["Grounding: iconic and categorical representations"]
  S --> DS["Distributional meaning: the company words keep"]
  DS --> O["Octopus argument: form alone lacks meaning"]
  DS --> CR["Conceptual role: meaning in relations"]
  O --> V["Vector grounding debate"]
  CR --> V
```

## Lecture

### The grounding problem

Harnad asked how the meanings of symbols in a formal system can be intrinsic to the system rather than parasitic on the meanings in the heads of its users [1]. He illustrated the problem with a dictionary-go-round. Someone who knows no Chinese and tries to learn it from a Chinese-Chinese dictionary will pass from one meaningless string to another without end. Every definition consists of further undefined symbols. The Chinese Room of Week 4 can be read as a case of the same problem.

Harnad proposed a hybrid solution. Elementary symbols are grounded in two kinds of non-symbolic representation. Iconic representations are analogues of sensory projections. Categorical representations are feature detectors that pick out the invariant properties of categories. Higher-level symbols are then composed from grounded ones, so that a new word such as zebra can inherit meaning from horse and stripes. Grounding, on this view, requires a causal connection between symbols and the things they are about.

<details>
<summary><b>Check your understanding.</b> What is the symbol grounding problem?</summary>

A. How symbols can be stored efficiently  
B. How the meanings of symbols can be intrinsic to a system rather than borrowed from the minds of interpreters  
C. How to translate between languages  
D. How to compress text  

**Answer: B.** Harnad compared the situation to learning Chinese from a Chinese-Chinese dictionary alone.

</details>

### Meaning from distribution

A different tradition locates meaning in patterns of use. Harris proposed that words that occur in similar contexts tend to have similar meanings [2]. Modern vector semantics turns the idea into computation. Each word is represented by the contexts in which it occurs. The co-occurrence counts are often weighted by positive pointwise mutual information, and their dimension is reduced. Figure 5.1 shows the result for a toy corpus: Animals, vehicles and fruits separate into regions, although the program has never seen an animal, a vehicle or a fruit. Large language models are distributional learners on an enormous scale, which is why the grounding problem has returned with new urgency.

![Toy corpus words positioned by their co-occurrence statistics alone. The categories separate even though the program has no access to animals, vehicles or fruits.](figures/w05_fig1.png)

*Figure 5.1. Toy corpus words positioned by their co-occurrence statistics alone. The categories separate even though the program has no access to animals, vehicles or fruits [2].*

<details>
<summary><b>Check your understanding.</b> What does the distributional hypothesis state?</summary>

A. Words are distributed randomly  
B. Meaning comes only from perception  
C. Words that occur in similar contexts tend to have similar meanings  
D. Word frequency determines meaning  

**Answer: C.** The hypothesis underlies word embeddings and language models.

</details>

### Form and meaning

Bender and Koller argued that a system trained only on linguistic form cannot learn meaning, understood as the relation between form and something outside language, such as communicative intent [3]. Their thought experiment features a hyperintelligent octopus that taps an undersea cable between two people stranded on separate islands. The octopus learns the statistical patterns of their messages well enough to impersonate one of them. When the other asks for help to build a device from local materials or to escape a bear, the octopus fails, because it has never had access to what the words are about.

Others resist the conclusion. Piantadosi and Hill argued that meaning need not depend on reference [4]. In conceptual role theories, the meaning of a concept is fixed by its relations to other concepts, and language models may capture such relations. Mollo and Millière distinguished several senses of grounding and argued that the relevant sense for language models is referential grounding, whose conditions do not require multimodal input or embodiment [5]. The debate turns on what meaning is, not only on what the models do.

<details>
<summary><b>Check your understanding.</b> What does Bender and Koller&#x27;s octopus argument claim?</summary>

A. Octopuses understand language  
B. A system trained only on linguistic form cannot learn meaning, understood as the relation between form and communicative intent  
C. Form and meaning are identical  
D. Language models are grounded by design  

**Answer: B.** The argument separates form from meaning and asks where meaning could come from.

</details>

### Grounding as a matter of degree

The positions can be compared by asking what connects symbols to the world in each case. For Harnad, the connection runs through perception. For distributional semantics, it runs through the texts that people wrote about the world, so it is indirect. For conceptual role theories, relations among concepts may carry part of the meaning even without reference. The interactive lab makes the contrast concrete. One part computes similarities from co-occurrence alone. Another part follows chains of definitions until they either loop or reach words marked as grounded in perception. The Colab notebook then tests whether a mapping learned from a few grounded words transfers to others.

> **Pause and reflect.** When a language model describes the taste of a lemon, is it referring to lemons? What would have to be added for the answer to change?

<details>
<summary><b>Check your understanding.</b> What does the view that grounding comes in degrees suggest?</summary>

A. Grounding is all or nothing  
B. Only humans are grounded  
C. Grounding requires consciousness  
D. Systems can be partly grounded through different routes, such as perception, action or relations to the world  

**Answer: D.** Graded views change the question from whether a system is grounded to how and how far.

</details>

## Interactive lab

Part A computes word similarities from a small corpus with a sliding context window. Part B follows the definitions of a toy dictionary. Without grounded words, the chains only return to other symbols. Marking some words as grounded in perception gives the chains an end [1, 2].

[Open the interactive lab](https://utkukose.github.io/philosophy-of-ai-NB-lecture/weeks/week-05/lab.html)

![Screenshot of the Week 5 interactive lab](screenshots/lab.png)

## Colab notebook

The Colab notebook builds distributional word vectors from a generated corpus and inspects their neighbourhoods. It then grounds a few words in simple perceptual features and tests whether the grounding transfers to words that were never grounded [1, 2, 5].

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/utkukose/philosophy-of-ai-NB-lecture/blob/main/weeks/week-05/NB05_symbol_grounding.ipynb)

Screenshots of the executed Colab notebook:

![Output 1 of the Week 5 Colab notebook](screenshots/nb_1.png)

## Self-assessment and reflection

The interactive lab contains a self-assessment of six questions (tab: Check yourself). Students answer each question, state how sure they are and receive instant feedback. A confident but wrong answer marks the first topic to revisit. The reflection prompts below also appear in the interactive lab (tab: Reflect and submit). Answers written there are saved in the browser and can be exported as a learning log.

1. Which position on meaning from this week do you find most plausible for language models, and what evidence would change your mind?
2. The Colab notebook transferred features from grounded to ungrounded words. Is that genuine grounding or a sophisticated dictionary-go-round?
3. Choose a technical term from your field. How did you come to understand it: through definitions, through use, through perception or through practice?

## Weekly task and submission

**What to do.** Compare two views of meaning and apply them to one case. First, state Harnad's grounding requirement: The symbols of a system have meaning for the system only if some of them are grounded in perception. Second, state the conceptual role view of Piantadosi and Hill: Meaning can come from the relations between concepts, even without reference. Third, choose one question from your field that a language model could answer. Explain what each view implies about whether the model understands its answer. Use at least one result of the Colab notebook as evidence.

**Where to look.** Lecture: sections "The grounding problem", "Form and meaning" and "Grounding as a matter of degree". Interactive lab: Part A for similarity from context and Part B for the dictionary-go-round. Colab notebook: Section 1 with Exercise 1, which finds the nearest neighbours of apple. Section 2 with Exercise 2 tests whether the edible feature transfers to words that were never grounded.

**Example.** A student of civil engineering could ask a language model which material suits a bridge in a cold climate. The model may answer well, because words such as steel and frost occur together in the texts it learned from. On Harnad's view, the model still does not know what steel is. On the conceptual role view, its web of relations may give its words a limited kind of meaning.

**What to submit.** About 500 words, and the Colab notebook with Exercises 1 and 2 completed.

The weekly task supports self-learning and builds a personal portfolio. In an active semester, students who follow the course with the instructor can send their work for evaluation to utkukose@sdu.edu.tr or utkukose@gmail.com. The e-mail contains the items that the task lists under What to submit. It also includes the learning log exported from the interactive lab (tab: Reflect and submit).

## Research and report assignment (optional)

**Do multimodal models ground their symbols?** Do models trained on images and text meet the conditions of the grounding requirement?

**What to do.** Examine whether multimodal models meet the conditions of Harnad's grounding requirement [1]. Contrast his view with the argument of Bender and Koller and with the vector grounding debate [3, 5].

**Where to start.** Lecture sections "The grounding problem", "Form and meaning" and "Grounding as a matter of degree". Section 2 of the Colab notebook shows a small form of grounding in perceptual features.

**Example focus.** A model that links the word red to red pixels in images has a connection to perception. The report could ask whether this connection is causal in Harnad's sense or only another correlation in data.

This research assignment is optional and supports self-learning. In an active semester, students who follow these weeks with the instructor can send the report for evaluation to utkukose@sdu.edu.tr or utkukose@gmail.com. The report has 1500 to 2500 words and follows the structure of an academic paper. It cites at least six scholarly or official sources in square brackets and ends with a reference list. The [report template](https://github.com/utkukose/philosophy-of-ai-NB-lecture/blob/main/exams/REPORT_TEMPLATE.md) shows a suitable structure.

## References

[1] Harnad, S. (1990). The symbol grounding problem. *Physica D: Nonlinear Phenomena*, 42(1-3), 335-346. <https://doi.org/10.1016/0167-2789(90)90087-6>

[2] Harris, Z. S. (1954). Distributional structure. *Word*, 10(2-3), 146-162. <https://doi.org/10.1080/00437956.1954.11659520>

[3] Bender, E. M., & Koller, A. (2020). Climbing towards NLU: On meaning, form, and understanding in the age of data. In *Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics* (pp. 5185-5198). <https://doi.org/10.18653/v1/2020.acl-main.463>

[4] Piantadosi, S. T., & Hill, F. (2022). Meaning without reference in large language models. arXiv preprint arXiv:2208.02957. <https://arxiv.org/abs/2208.02957>

[5] Mollo, D. C., & Millière, R. (2023). The vector grounding problem. arXiv preprint arXiv:2304.01481. <https://arxiv.org/abs/2304.01481>

---

<sub>Philosophy of Artificial Intelligence. Prof. Dr. Utku Kose, Süleyman Demirel University. ORCID [0000-0002-9652-6415](https://orcid.org/0000-0002-9652-6415). Content licensed under CC BY 4.0. This course is updated in line with current developments in the field. First version: September 2026. Last update: October 2026.</sub>
