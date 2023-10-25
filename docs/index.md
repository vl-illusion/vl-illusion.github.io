---
layout: default
---
## Intro

**Motivations**

- Humans are susceptible to visual illusions where we perceive things differently than physical reality 
- Do Vision-Language Models (VLMs), an emergent human-computer interface, also show similar phenomena? Or do they faithfully represent reality.

**In this work**

- We built [VL-Illusion](https://github.com/vl-illusion/dataset), a new dataset that systematically evaluate the problem.
- Through analysis, we found that alignment is low, larger models are closer to human perception and more susceptible to visual illusions.

**Abs**

Vision-Language Models (VLMs) are trained on vast amounts of data captured by humans emulating our understanding of the world. However, known as visual illusions, human's perception of reality isn't always faithful to the physical world. This raises a key question: do VLMs have the similar kind of illusions as humans do, or do they faithfully learn to represent reality? To investigate this question, we build a dataset containing five types of visual illusions and formulate four tasks to examine visual illusions in state-of-the-art VLMs.
Our findings have shown that although the overall alignment is low, larger models are closer to human perception and more susceptible to visual illusions. 
Our dataset and initial findings will promote a better understanding of visual illusions in humans and machines and provide a stepping stone for future computational models that can better align humans and machines in perceiving and communicating about the shared visual world. The code and data are available [here](https://github.com/vl-illusion/dataset).

## The VL-Illusion Dataset
The curated dataset contains over 1600 data points across five types of illusions and supports 4 different evaluation protocols.

## Results
### How well do models recognize illusions?
- In SameDiffQA, models more likely to not have illusions than recognize like humans
  - But larger models recognize illusions more
- Positive correlation between model scale and recognizing illusions

- 
