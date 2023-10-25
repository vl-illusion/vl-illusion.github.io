---
layout: default
---
## Do Vision-Language Models Perceive Illusions Like Humans?

**Motivations**

- Humans are susceptible to visual illusions where we perceive things differently than physical reality 
- Do Vision-Language Models (VLMs), an emergent human-computer interface, also show similar phenomena? Or do they faithfully represent reality.

**In this work**

- We built [VL-Illusion](https://github.com/vl-illusion/dataset), a new dataset that systematically evaluate the problem.
- Among all other exciting findings, we found that although the alignment between model and human's perception is low under illusion, larger models are more susceptible to visual illusions, and closer to human perception.


## The VL-Illusion Dataset
![ Example illusion from each category and the corresponding explanations](imgs/dataset_types.png)

The curated dataset contains over 1600 data points across five types of illusions and supports 4 different evaluation protocols.

![Example illustration for each task setup. Left:SameDiff QA. Right: RefQA, AttrQA, RefLoc](imgs/dataset_tasks.png)


## Experiments and Results
We evaluate four representative models, LLaVA, InstructBLIP, Unified-IO and OFA on the VL-Illusion dataset. Please refer to the paper for more details.

### How Well Do Models Recognize Illusions?
Firstly,

![1](imgs/1.png)
- Under SameDiff-QA task, which specially challenges the ability to recognize illusions, models more likely to not have illusions compared to recognize like humans.
- But we do confirm that there's a positive correlation between model scale and the ability to recognize illusions

### How Alined Are Models Under Illusion?
![2](imgs/2.png)

We find the answer to be complex and model's performance varies significantly across different task formulations.

For example, the alignment score is quite low on RefQA and AttrQA tasks, but the alignment score is much higher on RefLoc task.

Again, we confirm that larger models consistently align better with human perception.

## Does Alignment Vary By Illusion Type?
![3](imgs/3.png)

Yes, we found that the alignment score varies significantly across different illusion types. Color constancy illusion is the most challenging one for models, while the alignment score is much higher for the perspective illusion.