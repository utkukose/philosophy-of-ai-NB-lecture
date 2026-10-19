<div align="center">

# Final Capstone: Minds, Morals and Machines

**Philosophy of Artificial Intelligence (11118BLG003)**  
Prof. Dr. Utku Kose, Süleyman Demirel University

[![Course home](https://img.shields.io/badge/course-home-B97813)](../../README.md)

</div>

## Overview

The final capstone integrates Weeks 8 to 14: the frame problem and common sense, the limits of machines, consciousness and its science, understanding and world models, creativity and intentionality [1, 2, 3, 4]. Students choose the research track or the application track.

## Formats

Two tracks are available. In the research track, the capstone is an academic text of 3500 to 5000 words. It defends a thesis on one of the suggested topics or on a related topic approved by the instructor. It engages with at least ten scholarly sources and answers the strongest objection to its thesis. In the application track, the capstone extends one of the three example Colab notebooks. A report of 2500 to 4000 words connects the computational results to the philosophical question. Each student works individually. The weights below are indicative; in active semesters the instructor confirms them at the start of the semester.

## How to work on this capstone

Both tracks are assessed with the same criteria, which are listed below. The research track suits students who want to build and defend an argument. The application track suits students who want to extend a simulation and interpret its results.

### Research track

**Step 1. Choose a topic.** Pick one of the suggested research topics below, or propose a related topic to the instructor. The week in brackets after each topic shows where the course treats it.

**Step 2. Read.** Reread the lecture of the week or weeks named after the topic. Collect at least ten scholarly sources, starting from the references of those lectures.

**Step 3. Build the argument.** State a thesis. Reconstruct the main arguments for and against it as numbered premises and conclusions.

**Step 4. Write.** Write the text with the course report template, and answer the strongest objection to your thesis.

**Step 5. Submit.** Send the text as a PDF file. The submission section below gives the deadline for active semesters.

### Application track

**Step 1. Choose a project.** Pick one of the three advanced application projects below. The related weeks of each project show which lecture pages, interactive labs and Colab notebooks to revisit.

**Step 2. Run the example.** Open the example Colab notebook of the project with its badge. Save a copy to your own Google Drive (File, Save a copy in Drive), run all cells from top to bottom and read what the baseline implements.

**Step 3. Extend it.** Implement every required extension in your copy. Fix the random seeds so that another person can reproduce the results.

**Step 4. Evaluate and write.** Compare the extensions with the baseline and write the report with the course report template. Explain what the results can and cannot show about the philosophical question.

**Step 5. Submit.** Send the report as a PDF file and a link to your Colab notebook with view access. The submission section below gives the deadline for active semesters.

## Suggested research topics

The titles below are starting points. Students may narrow a title or propose a related one that fits the scope of the capstone.

1. Is the frame problem solved, dissolved or merely hidden in large language models? (Week 8)
2. The Lucas-Penrose argument: What survives the consistency objection? (Week 9)
3. Indicator properties and machine consciousness: Strengths and limits of the theory-heavy approach (Week 11)
4. Integrated information and artificial systems: Why the hardware might matter (Week 11)
5. Biological naturalism versus computational functionalism in the debate on conscious AI (Weeks 10 and 11)
6. World models in sequence models: What interventions show and what they do not (Week 12)
7. Formal and functional competence: A philosophical reading of the dissociation thesis (Week 12)
8. Can machines be creative? Boden's categories applied to generative AI (Week 13)
9. The intentional stance towards language model agents: Prediction, attribution and misattribution (Week 14)
10. Moral judgement in language models: An intrinsic property or a product of prompting and context? (Weeks 12 and 14)

## Advanced application projects

Each project comes with an example Colab notebook that implements a working baseline. The capstone extends the baseline as described, evaluates the extensions and reports the results.

### Project 1: Moral judgement under framing: Is machine morality intrinsic or induced?

**Related weeks.** Weeks 12 and 14. Lecture: section "Talking about language models" of Week 12, and sections "The mark of the mental" and "The intentional stance" of Week 14.

A factorial experiment probes the decisions and justifications of a respondent across eight dilemmas, four framings, two orders of the answer options, three paraphrases and four sessions. It measures consistency across paraphrases, sensitivity to framing, order effects, the vocabulary of justifications and drift across sessions. The design is inspired by an earlier open framework on moral decision-making in language models [5], with new dilemmas, factors and measures. To run offline, the example uses a transparent simulated respondent with known parameters.

**Required extensions.** Connect a real language model, either through an API with the key kept in an environment variable or as an open model run locally. Run the full design with enough repetitions for the statistical tests, and justify the number with a power calculation. Add at least one measure of justification quality beyond vocabulary, for example agreement with human raters. Then argue in the report whether the observed behaviour supports attributing moral judgement to the system. Use the intentional stance and the distinction between original and derived intentionality [4, 6, 7].

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/utkukose/philosophy-of-ai-NB-lecture/blob/main/exams/final/FIN1_moral_judgement_framing.ipynb) Example Colab notebook: `FIN1_moral_judgement_framing.ipynb`

![Output of the example Colab notebook](screenshots/FIN1_moral_judgement_framing_1.png)
![Output of the example Colab notebook](screenshots/FIN1_moral_judgement_framing_2.png)

### Project 2: Integration, broadcast and indicator properties in small networks

**Related weeks.** Week 11. Lecture: sections "Global workspace theories", "Integrated information theory" and "Indicator properties and the debate about AI". Interactive lab: Part B, which computes a simplified integration measure. Colab notebook: Sections 1 and 2.

The simplified integration measure of Week 11 is computed for hundreds of random Boolean networks with and without feedback. A workspace of competing modules is then simulated to study ignition and global availability [8, 9].

**Required extensions.** Test systematically whether recurrence is necessary and sufficient for positive integration in the simplified measure, and explain the exceptions. Compare the measure with a second one from the literature [10]. Build a small architecture that satisfies indicator properties of two theories at once and discuss what, if anything, the exercise shows about consciousness [3, 11].

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/utkukose/philosophy-of-ai-NB-lecture/blob/main/exams/final/FIN2_integration_and_workspace.ipynb) Example Colab notebook: `FIN2_integration_and_workspace.ipynb`

![Output of the example Colab notebook](screenshots/FIN2_integration_and_workspace_1.png)

### Project 3: Theory of mind and misattribution: When is the intentional stance a real pattern?

**Related weeks.** Week 14. Lecture: sections "The intentional stance" and "Attributing minds". Interactive lab: Part B on inverse planning. Colab notebook: Sections 1 and 2.

An observer infers goals by Bayesian inverse planning from the moves of four kinds of agents: goal-directed agents, random walkers, rule-following wall followers and chasers that pursue a moving target [12, 13]. The experiment measures how often goals are attributed and how many bits per move each stance needs to describe the behaviour, a compression reading of Dennett's real patterns [14].

**Required extensions.** Add a design stance that knows the rules of each agent, agents with changing goals, and observers with different priors. Identify the conditions under which attributing goals is a misattribution, and argue in the report how the results bear on attributing beliefs and desires to language model agents [7].

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/utkukose/philosophy-of-ai-NB-lecture/blob/main/exams/final/FIN3_theory_of_mind_attribution.ipynb) Example Colab notebook: `FIN3_theory_of_mind_attribution.ipynb`

![Output of the example Colab notebook](screenshots/FIN3_theory_of_mind_attribution_1.png)

## Report

Both tracks follow the course report template. A research report states its thesis in the introduction, reconstructs the relevant arguments as explicit premises and conclusions, and evaluates them. An application report explains what the simulation or experiment can and cannot show about the philosophical question, presents its results with figures and discusses its limitations. All sources are cited in square brackets.

A common structure for reports is given in the [report template](https://github.com/utkukose/philosophy-of-ai-NB-lecture/blob/main/exams/REPORT_TEMPLATE.md).

## Assessment criteria

| Criterion | Weight | What is assessed |
|---|---|---|
| Thesis and argument | 30% | A clear thesis supported by a valid and well-structured argument. |
| Engagement with the literature | 25% | Accurate reconstruction of the positions and replies discussed in the course and beyond. |
| Critical evaluation and originality | 20% | Objections are anticipated and answered; the text adds a considered view of its own. |
| Evidence and method | 15% | Research track: depth of analysis. Application track: correctness and reproducibility of the Colab notebook. |
| Writing and referencing | 10% | The text is clear, concise and correctly referenced. |

## Submission

This capstone also supports self-learning and can be completed at any pace. In an active semester, the final capstone is sent by e-mail to utkukose@sdu.edu.tr or utkukose@gmail.com. The deadline is 23:53 (Türkiye time) on the Sunday that ends Week 14. The e-mail contains the report as a PDF file. In the application track, it also contains a link to the Colab notebook.

## References

[1] Dennett, D. C. (1984). Cognitive wheels: The frame problem of AI. In C. Hookway (Eds.), *Minds, Machines and Evolution* (pp. 129-151). Cambridge University Press.

[2] Chalmers, D. J. (1995). Facing up to the problem of consciousness. *Journal of Consciousness Studies*, 2(3), 200-219.

[3] Butlin, P., Long, R., Elmoznino, E., Bengio, Y., Birch, J., Constant, A., Deane, G., Fleming, S. M., Frith, C., Ji, X., Kanai, R., Klein, C., Lindsay, G., Michel, M., Mudrik, L., Peters, M. A. K., Schwitzgebel, E., Simon, J., & VanRullen, R. (2023). Consciousness in artificial intelligence: Insights from the science of consciousness. arXiv preprint arXiv:2308.08708. <https://arxiv.org/abs/2308.08708>

[4] Dennett, D. C. (1987). *The Intentional Stance*. MIT Press.

[5] Kose, U. (2026). *MoralLLM-Lab: An experimental framework on moral decision-making in large language models*. <https://github.com/utkukose/MoralLLM-Lab>

[6] Searle, J. R. (1983). *Intentionality: An Essay in the Philosophy of Mind*. Cambridge University Press.

[7] Shanahan, M. (2024). Talking about large language models. *Communications of the ACM*, 67(2), 68-79. <https://doi.org/10.1145/3624724>

[8] Tononi, G. (2004). An information integration theory of consciousness. *BMC Neuroscience*, 5, 42. <https://doi.org/10.1186/1471-2202-5-42>

[9] Dehaene, S., & Naccache, L. (2001). Towards a cognitive neuroscience of consciousness: Basic evidence and a workspace framework. *Cognition*, 79(1-2), 1-37. <https://doi.org/10.1016/S0010-0277(00)00123-2>

[10] Albantakis, L., Barbosa, L., Findlay, G., et al. (2023). Integrated information theory (IIT) 4.0: Formulating the properties of phenomenal existence in physical terms. *PLOS Computational Biology*, 19(10), e1011465. <https://doi.org/10.1371/journal.pcbi.1011465>

[11] Seth, A. K. (2025). Conscious artificial intelligence and biological naturalism. *Behavioral and Brain Sciences*. Published online 21 April 2025. <https://doi.org/10.1017/S0140525X25000032>

[12] Baker, C. L., Saxe, R., & Tenenbaum, J. B. (2009). Action understanding as inverse planning. *Cognition*, 113(3), 329-349. <https://doi.org/10.1016/j.cognition.2009.07.005>

[13] Heider, F., & Simmel, M. (1944). An experimental study of apparent behavior. *The American Journal of Psychology*, 57(2), 243-259. <https://doi.org/10.2307/1416950>

[14] Dennett, D. C. (1991). Real patterns. *The Journal of Philosophy*, 88(1), 27-51. <https://doi.org/10.2307/2027085>

---

<sub>Philosophy of Artificial Intelligence. Prof. Dr. Utku Kose, Süleyman Demirel University. ORCID [0000-0002-9652-6415](https://orcid.org/0000-0002-9652-6415). Content licensed under CC BY 4.0. This course is updated in line with current developments in the field. First version: September 2026. Last update: October 2026.</sub>
