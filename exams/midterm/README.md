<div align="center">

# Midterm Capstone: Machines, Tests and Meaning

**Philosophy of Artificial Intelligence (11118BLG003)**  
Prof. Dr. Utku Kose, Süleyman Demirel University

[![Course home](https://img.shields.io/badge/course-home-B97813)](../../README.md)

</div>

## Overview

The midterm capstone integrates Weeks 1 to 7: definitions and measures of intelligence, the Turing test, computation and functionalism, the Chinese Room, symbol grounding, systematicity and embodiment [1, 2, 3, 4]. Students choose the research track or the application track.

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

1. Does passing a three-party Turing test show that a system thinks? The 2025 results in the light of Block and French (Week 2)
2. The Chinese Room and large language models: Which reply survives? (Week 4)
3. Symbol grounding without sensors: Can distributional learning fix reference? (Week 5)
4. Multiple realisability and the question of the substrate for artificial minds (Week 3)
5. Systematicity revisited: What meta-learning shows about the challenge of Fodor and Pylyshyn (Week 6)
6. Embodiment as a condition for intelligence: Brooks, the enactivists and disembodied language models (Week 7)
7. Psychologism and behaviourism: Is the way behaviour is produced part of what intelligence is? (Week 2)
8. Measuring intelligence: Legg and Hutter, Chollet and the problem of benchmarks (Week 1)
9. The extended mind and AI tools: Is a language model part of its user's cognitive system? (Week 7)
10. Is computation observer-relative? Searle, Putnam and the mechanistic account (Week 3)

## Advanced application projects

Each project comes with an example Colab notebook that implements a working baseline. The capstone extends the baseline as described, evaluates the extensions and reports the results.

### Project 1: An imitation game laboratory

**Related weeks.** Week 2. Lecture: sections "Is behaviour enough?" and "The test in the age of language models". Interactive lab: Part A, where you act as the interrogator. Colab notebook: Sections 1 to 3, on ELIZA, on interrogators and on judges compared with chance.

Two machine witnesses, a pattern-matching program in the style of ELIZA and a Markov chain trained on a small corpus, play three-party games against constructed human replies. A learned interrogator judges the replies from surface cues, and the results are analysed with exact power calculations and Bayesian estimates of the win rate [1, 5, 6].

**Required extensions.** Add a stronger witness, for example a retrieval-based responder or a small language model, and at least two further cues or a text classifier as interrogator. Determine how many games are needed to test Turing's 70 percent criterion reliably. In the report, argue what the win rates can and cannot show, with reference to Blockhead and to subcognitive questions [7, 8].

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/utkukose/philosophy-of-ai-NB-lecture/blob/main/exams/midterm/MID1_imitation_game_lab.ipynb) Example Colab notebook: `MID1_imitation_game_lab.ipynb`

![Output of the example Colab notebook](screenshots/MID1_imitation_game_lab_1.png)

### Project 2: Grounding through language games

**Related weeks.** Week 5. Lecture: sections "The grounding problem", "Form and meaning" and "Grounding as a matter of degree". Colab notebook: Section 2, where a few words are grounded in perception.

A population of agents invents and aligns a vocabulary for colours, sizes and shapes by playing naming games about objects they perceive. The vocabulary is then studied as text only: Co-occurrence recovers the dimensions of meaning, but reference stays at chance unless some words are grounded [3, 9].

**Required extensions.** Add perceptual noise and continuous features, so that categories must be learned rather than given. Compare populations of different sizes. Test whether structural information can propagate reference from anchor words to other words. Discuss what the results imply for conceptual role semantics and for the vector grounding debate [10, 11].

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/utkukose/philosophy-of-ai-NB-lecture/blob/main/exams/midterm/MID2_grounding_naming_game.ipynb) Example Colab notebook: `MID2_grounding_naming_game.ipynb`

![Output of the example Colab notebook](screenshots/MID2_grounding_naming_game_1.png)
![Output of the example Colab notebook](screenshots/MID2_grounding_naming_game_2.png)

### Project 3: Evolving Braitenberg vehicles

**Related weeks.** Week 7. Lecture: sections "Synthetic psychology" and "The embodied and enactive mind". Interactive lab: the Braitenberg vehicle. Colab notebook: Section 1.

Instead of wiring vehicles by hand, a genetic algorithm evolves sensor-motor weights and the angle of the sensors for two tasks: approaching a light and keeping a fixed distance from it. The evolved controllers are then analysed in Braitenberg's terms, which illustrates the difference between downhill invention and uphill analysis [12, 13].

**Required extensions.** Add a second light with a different colour and sensors for each colour. Evolve controllers that approach one light while avoiding the other. Study how the sensor angle, a property of the body, co-evolves with the wiring. Discuss whether observers' descriptions in terms of fear or love are justified and what the results imply for embodied accounts of cognition [4, 14].

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/utkukose/philosophy-of-ai-NB-lecture/blob/main/exams/midterm/MID3_evolving_vehicles.ipynb) Example Colab notebook: `MID3_evolving_vehicles.ipynb`

![Output of the example Colab notebook](screenshots/MID3_evolving_vehicles_1.png)

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

This capstone also supports self-learning and can be completed at any pace. In an active semester, the midterm capstone is sent by e-mail to utkukose@sdu.edu.tr or utkukose@gmail.com. The deadline is 23:53 (Türkiye time) on the Sunday that ends Week 7. The e-mail contains the report as a PDF file. In the application track, it also contains a link to the Colab notebook.

## References

[1] Turing, A. M. (1950). Computing machinery and intelligence. *Mind*, 59(236), 433-460. <https://doi.org/10.1093/mind/LIX.236.433>

[2] Searle, J. R. (1980). Minds, brains, and programs. *Behavioral and Brain Sciences*, 3(3), 417-424. <https://doi.org/10.1017/S0140525X00005756>

[3] Harnad, S. (1990). The symbol grounding problem. *Physica D: Nonlinear Phenomena*, 42(1-3), 335-346. <https://doi.org/10.1016/0167-2789(90)90087-6>

[4] Brooks, R. A. (1991). Intelligence without representation. *Artificial Intelligence*, 47(1-3), 139-159. <https://doi.org/10.1016/0004-3702(91)90053-M>

[5] Weizenbaum, J. (1966). ELIZA: A computer program for the study of natural language communication between man and machine. *Communications of the ACM*, 9(1), 36-45. <https://doi.org/10.1145/365153.365168>

[6] Jones, C. R., & Bergen, B. K. (2025). Large language models pass the Turing test. arXiv preprint arXiv:2503.23674. <https://arxiv.org/abs/2503.23674>

[7] Block, N. (1981). Psychologism and behaviorism. *The Philosophical Review*, 90(1), 5-43. <https://doi.org/10.2307/2184371>

[8] French, R. M. (1990). Subcognition and the limits of the Turing test. *Mind*, 99(393), 53-65. <https://doi.org/10.1093/mind/XCIX.393.53>

[9] Piantadosi, S. T., & Hill, F. (2022). Meaning without reference in large language models. arXiv preprint arXiv:2208.02957. <https://arxiv.org/abs/2208.02957>

[10] Mollo, D. C., & Millière, R. (2023). The vector grounding problem. arXiv preprint arXiv:2304.01481. <https://arxiv.org/abs/2304.01481>

[11] Bender, E. M., & Koller, A. (2020). Climbing towards NLU: On meaning, form, and understanding in the age of data. In *Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics* (pp. 5185-5198). <https://doi.org/10.18653/v1/2020.acl-main.463>

[12] Braitenberg, V. (1984). *Vehicles: Experiments in Synthetic Psychology*. MIT Press.

[13] Pfeifer, R., & Bongard, J. (2006). *How the Body Shapes the Way We Think: A New View of Intelligence*. MIT Press.

[14] Varela, F. J., Thompson, E., & Rosch, E. (1991). *The Embodied Mind: Cognitive Science and Human Experience*. MIT Press.

---

<sub>Philosophy of Artificial Intelligence. Prof. Dr. Utku Kose, Süleyman Demirel University. ORCID [0000-0002-9652-6415](https://orcid.org/0000-0002-9652-6415). Content licensed under CC BY 4.0. This course is updated in line with current developments in the field. First version: September 2026. Last update: October 2026.</sub>
