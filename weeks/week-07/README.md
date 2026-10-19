<div align="center">

# Week 07: Embodiment, Situatedness and the Extended Mind

**Philosophy of Artificial Intelligence (11118BLG003)**  
Prof. Dr. Utku Kose, Süleyman Demirel University

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/utkukose/philosophy-of-ai-NB-lecture/blob/main/weeks/week-07/NB07_embodiment.ipynb) [![Interactive lab](https://img.shields.io/badge/interactive%20lab-open-1D5B78)](https://utkukose.github.io/philosophy-of-ai-NB-lecture/weeks/week-07/lab.html) [![Lecture notes](https://img.shields.io/badge/lecture%20notes-PDF-566A73)](Week07_Lecture_Notes.pdf) [![Course home](https://img.shields.io/badge/course-home-B97813)](../../README.md)

</div>

## Overview

Classical AI treated intelligence as reasoning over internal representations. This week examines the alternative that intelligence arises from bodies acting in environments: behaviour-based robotics, Braitenberg's synthetic psychology, enactivism and the thesis that the mind extends beyond the skull [1, 2, 3].

**Estimated study time:** 6 to 8 hours.

## Learning outcomes

By the end of the week, students are expected to explain Brooks's case against central representation and the subsumption architecture. They should be able to derive the behaviour of Braitenberg vehicles from their wiring and to describe the enactive and morphological views of cognition. Finally, they should be able to evaluate the parity argument for the extended mind.

## Study path

| Step | Activity | Suggested time |
|---|---|---|
| 1 | Read the lecture below or the [PDF version](Week07_Lecture_Notes.pdf) | 90 minutes |
| 2 | Explore the [interactive lab](https://utkukose.github.io/philosophy-of-ai-NB-lecture/weeks/week-07/lab.html) | 45 minutes |
| 3 | Work through the [Colab notebook](https://colab.research.google.com/github/utkukose/philosophy-of-ai-NB-lecture/blob/main/weeks/week-07/NB07_embodiment.ipynb) and its exercises | 2 to 3 hours |
| 4 | Take the self-assessment in the interactive lab (tab: Check yourself) | 20 minutes |
| 5 | Answer the reflection prompts in the interactive lab, export the learning log and complete the weekly task | 60 minutes |

## Week at a glance

```mermaid
flowchart LR
  B["Brooks: behaviour-based robots, no central model"] --> SUB["Subsumption layers"]
  MV["Moravec's paradox"] --> B
  BR["Braitenberg vehicles"] --> SP["Synthetic psychology: easy to build, hard to analyse"]
  EN["Enaction: cognition as structural coupling"] --> MC["Morphological computation"]
  EX["Extended mind: parity principle"] --> OT["Otto's Colab notebook"]
```

## Lecture

### Intelligence without representation

Brooks argued that AI had focused on the wrong problems [1]. Instead of building disembodied reasoners with central world models, researchers should build complete creatures that act in the real world, starting with simple behaviours and adding layers. In his subsumption architecture, each layer connects perception directly to action, such as avoiding obstacles or wandering, and higher layers can suppress or override lower ones. The robots used the world itself as their source of information instead of maintaining detailed internal models.

Moravec observed a related asymmetry, often called Moravec's paradox [4]. Tasks that people find intellectually hard, such as chess, turned out to be comparatively easy for computers. Tasks that people find effortless, such as perceiving and moving, turned out to be very hard. Evolution spent far longer refining sensorimotor skills than abstract reasoning.

<details>
<summary><b>Check your understanding.</b> What characterises Brooks&#x27;s subsumption architecture?</summary>

A. A central world model and a planner  
B. Layers of simple behaviours coupled directly to sensing and acting, without a central world model  
C. Symbolic theorem proving  
D. Pure reinforcement learning  

**Answer: B.** Brooks argued that the world is its own best model.

</details>

### Synthetic psychology

Braitenberg described a series of imaginary vehicles, each with sensors connected to motors by simple wiring [2]. A vehicle with two light sensors, each driving the wheel on its own side more strongly when light is brighter, turns away from light and seems to fear it. Crossing the wires makes it turn towards the light and rush at it, as if aggressive. With inhibitory connections, the uncrossed vehicle approaches the light and slows down, facing it as if in love. The crossed one approaches and then turns away, like an explorer. Figure 7.1 shows these trajectories.

Braitenberg drew a methodological moral, the law of uphill analysis and downhill invention: It is easier to build a mechanism that produces a behaviour than to infer the mechanism from the behaviour. Observers readily attribute emotions and intentions to the vehicles, even though the mechanism is transparent to the designer. The interactive lab lets students rewire the vehicles and change their morphology, and Week 14 returns to the attribution of intentions.

![Trajectories of four Braitenberg vehicles that differ only in whether their sensor-motor connections are crossed and whether they excite or inhibit.](figures/w07_fig1.png)

*Figure 7.1. Trajectories of four Braitenberg vehicles that differ only in whether their sensor-motor connections are crossed and whether they excite or inhibit [2].*

<details>
<summary><b>Check your understanding.</b> What is Braitenberg&#x27;s law of uphill analysis and downhill invention?</summary>

A. Analysis is always easier than synthesis  
B. Vehicles should drive downhill  
C. Behaviour cannot be analysed  
D. It is easier to build a mechanism that produces behaviour than to infer the mechanism from the behaviour  

**Answer: D.** Simple wiring can produce behaviour that observers describe in rich psychological terms.

</details>

### The embodied and enactive mind

Varela, Thompson and Rosch proposed that cognition is enaction [5]. Enaction is the bringing forth of a world through the history of structural coupling between an organism and its environment, grounded in sensorimotor capacities. Cognition, on this view, is not the representation of a pre-given world by a pre-given mind. Pfeifer and Bongard developed the engineering side of the idea [6]. They argued that the shape and material of a body take over part of the work that would otherwise require computation. They called this phenomenon morphological computation. A change in the angle of a vehicle's sensors, as in the interactive lab, can change its behaviour as much as a change in its wiring.

<details>
<summary><b>Check your understanding.</b> What does enactivism claim?</summary>

A. Cognition arises from the dynamic interaction of an embodied agent with its environment  
B. Cognition is computation over internal symbols  
C. The body is irrelevant to the mind  
D. Only language matters  

**Answer: A.** Enactivism emphasises sense-making in activity rather than internal representation.

</details>

### The extended mind

Clark and Chalmers asked where the mind stops and the rest of the world begins [3]. Their example contrasts Inga, who remembers the address of a museum, with Otto, who has a memory impairment and consults a Colab notebook he always carries. They proposed a parity principle. If a part of the world functions as a process that we would call cognitive if it occurred in the head, then that part of the world is part of the cognitive process. Otto's Colab notebook, on this view, is part of his memory.

The thesis raises questions about AI systems that rely on external tools and stores, and about people who rely on AI systems. Critics object that the Colab notebook lacks the integration and automatic trust that mark biological memory. The Colab notebook of this week simulates agents with limited internal memory that can consult an external store, which makes the parity principle a question about performance and cost.

> **Pause and reflect.** Is a search engine you consult daily part of your memory in the sense of Clark and Chalmers? Which of their conditions does it meet?

<details>
<summary><b>Check your understanding.</b> According to the extended mind thesis, when can a Colab notebook be part of a cognitive process?</summary>

A. Never  
B. Only if it is digital  
C. When it is reliably available and trusted and plays the role memory would play  
D. Only for experts  

**Answer: C.** Clark and Chalmers argued from the parity between Otto's Colab notebook and biological memory.

</details>

## Interactive lab

Choose the wiring of a two-sensor vehicle, move the light and change the angle of the sensors. Scrub through time to follow the vehicle. The label on each wiring is the emotion that Braitenberg suggested an observer would attribute [2, 6].

[Open the interactive lab](https://utkukose.github.io/philosophy-of-ai-NB-lecture/weeks/week-07/lab.html)

![Screenshot of the Week 7 interactive lab](screenshots/lab.png)

## Colab notebook

The Colab notebook simulates Braitenberg vehicles and builds a small subsumption controller whose layers can be switched on and off. It also models an agent with limited internal memory that can consult an external store, in the spirit of the parity principle [1, 2, 3].

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/utkukose/philosophy-of-ai-NB-lecture/blob/main/weeks/week-07/NB07_embodiment.ipynb)

Screenshots of the executed Colab notebook:

![Output 1 of the Week 7 Colab notebook](screenshots/nb_1.png)

## Self-assessment and reflection

The interactive lab contains a self-assessment of six questions (tab: Check yourself). Students answer each question, state how sure they are and receive instant feedback. A confident but wrong answer marks the first topic to revisit. The reflection prompts below also appear in the interactive lab (tab: Reflect and submit). Answers written there are saved in the browser and can be exported as a learning log.

1. Which Braitenberg vehicle surprised you most, and which descriptions came to mind before you checked the wiring?
2. Could a language model without a body be intelligent in the sense of Brooks or the enactivists? Give their likely answers and your own.
3. Identify a tool in your research practice that might count as part of your extended mind. Which conditions of Clark and Chalmers does it meet?

## Weekly task and submission

**What to do.** Apply the embodied and extended views of cognition to one AI system of your choice. First, describe the body of the system, its sensors, its environment and the tools or stores it uses. Second, apply two views of this week, for example Brooks's case against central representation and the parity principle of the extended mind. Third, decide where the intelligence of the system is located: in the model, the body, the environment or their coupling. Use one result of the interactive lab or the Colab notebook as an example.

**Where to look.** Lecture: sections "Intelligence without representation", "Synthetic psychology", "The embodied and enactive mind" and "The extended mind". Interactive lab: the Braitenberg vehicle, whose wiring and sensor angle you choose (tab: Explore). Colab notebook: Section 2 for the subsumption controller and Section 3 for memory inside and outside the head.

**Example.** A robot vacuum cleaner avoids walls mainly through its round body and its bump sensors, with little central planning. Under the parity principle, the map of the flat stored in its app could count as part of its cognitive process. Its intelligence would then lie in the coupling of controller, body and environment.

**What to submit.** About 500 words, and the Colab notebook with Exercises 1 and 2 completed. The midterm capstone, which also ends this week, is a separate piece of work.

The weekly task supports self-learning and builds a personal portfolio. In an active semester, students who follow the course with the instructor can send their work for evaluation to utkukose@sdu.edu.tr or utkukose@gmail.com. The e-mail contains the items that the task lists under What to submit. It also includes the learning log exported from the interactive lab (tab: Reflect and submit).

## Research and report assignment (optional)

**Embodiment in the age of foundation models.** Do robots controlled by large pretrained models support the embodied view of cognition?

**What to do.** Evaluate whether robots controlled by large pretrained models vindicate or challenge the embodied and enactive views of cognition [1, 5, 6]. Consider both the body of the robot and the training of the model on text and images.

**Where to start.** Lecture sections "Intelligence without representation" and "The embodied and enactive mind".

**Example focus.** A robot that plans with a language model but acts through learned motor skills combines central representation with bodily control. The report could ask which part does the work that Brooks thought representation could not do.

This research assignment is optional and supports self-learning. In an active semester, students who follow these weeks with the instructor can send the report for evaluation to utkukose@sdu.edu.tr or utkukose@gmail.com. The report has 1500 to 2500 words and follows the structure of an academic paper. It cites at least six scholarly or official sources in square brackets and ends with a reference list. The [report template](https://github.com/utkukose/philosophy-of-ai-NB-lecture/blob/main/exams/REPORT_TEMPLATE.md) shows a suitable structure.

## Midterm capstone

This week closes the first half of the course with the [Midterm Capstone: Machines, Tests and Meaning](../../exams/midterm/README.md).

This capstone also supports self-learning and can be completed at any pace. In an active semester, the midterm capstone is sent by e-mail to utkukose@sdu.edu.tr or utkukose@gmail.com. The deadline is 23:53 (Türkiye time) on the Sunday that ends Week 7. The e-mail contains the report as a PDF file. In the application track, it also contains a link to the Colab notebook.

## References

[1] Brooks, R. A. (1991). Intelligence without representation. *Artificial Intelligence*, 47(1-3), 139-159. <https://doi.org/10.1016/0004-3702(91)90053-M>

[2] Braitenberg, V. (1984). *Vehicles: Experiments in Synthetic Psychology*. MIT Press.

[3] Clark, A., & Chalmers, D. (1998). The extended mind. *Analysis*, 58(1), 7-19. <https://doi.org/10.1093/analys/58.1.7>

[4] Moravec, H. (1988). *Mind Children: The Future of Robot and Human Intelligence*. Harvard University Press.

[5] Varela, F. J., Thompson, E., & Rosch, E. (1991). *The Embodied Mind: Cognitive Science and Human Experience*. MIT Press.

[6] Pfeifer, R., & Bongard, J. (2006). *How the Body Shapes the Way We Think: A New View of Intelligence*. MIT Press.

---

<sub>Philosophy of Artificial Intelligence. Prof. Dr. Utku Kose, Süleyman Demirel University. ORCID [0000-0002-9652-6415](https://orcid.org/0000-0002-9652-6415). Content licensed under CC BY 4.0. This course is updated in line with current developments in the field. First version: September 2026. Last update: October 2026.</sub>
