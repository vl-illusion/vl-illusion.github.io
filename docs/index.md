---
layout: default
---
## Intro

**Motivations**

- Humans are susceptible to visual illusions where we perceive things differently than physical reality 
- Do Vision-Language Models (VLMs), an emergent human-computer interface, also show similar phenomena? Or do they faithfully represent reality.

**In this work**

- We built [VL-Illusion](https://github.com/vl-illusion/dataset), a new dataset that systematically evaluate the problem.
- Through analysis, we found that although the alignment between model and human's perception is low under illusion, larger models are more susceptible to visual illusions, and closer to human perception.

**Abs**

Vision-Language Models (VLMs) are trained on vast amounts of data captured by humans emulating our understanding of the world. However, known as visual illusions, human's perception of reality isn't always faithful to the physical world. This raises a key question: do VLMs have the similar kind of illusions as humans do, or do they faithfully learn to represent reality? To investigate this question, we build a dataset containing five types of visual illusions and formulate four tasks to examine visual illusions in state-of-the-art VLMs.
Our findings have shown that although the overall alignment is low, larger models are closer to human perception and more susceptible to visual illusions. 
Our dataset and initial findings will promote a better understanding of visual illusions in humans and machines and provide a stepping stone for future computational models that can better align humans and machines in perceiving and communicating about the shared visual world. The code and data are available [here](https://github.com/vl-illusion/dataset).

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