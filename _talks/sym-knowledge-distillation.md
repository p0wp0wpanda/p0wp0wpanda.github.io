---
title: "Symbolic Knowledge Distillation"
collection: talks
permalink: /talks/sym-knowledge
date: 2023-10-06
---

This paper presents a unique approach to distilling the knowledge baked into general purpose, large LMs into smaller, in a way more 'concentrated' networks.
In their particular use case, they focus on building a smaller, distilled, commonsense network that is able to outperform GPT-3 on causal commonsense tasks

The paper posits that finetuning large networks like GPT-3 requires a large amount of accurate, labelled data which is expensive to acquire. Instead the propose
a 'student-teacher' model where the general purpose model (in this case GPT-3) can, with precise prompting, automatically generate a large number of
training examples that conform closely with what we want to train the distilled model with. They do this in the form of a knowledge graph.

The authors go on to show that their generated knowledge graph ${ATOMIC}^{10x}$ is
  - Significantly larger than comparable human-generated knowledge graphs
  - Almost the same quality as the human-generated versions (Even higher quality if a 'critic' network is used to filter the general LLMs outputs)
  - More unique than the human-generated versions by word uniqueness metrics


The authors call this methodology $machine \rightarrow corpus \rightarrow machine$ distillation. The knowledge graph they ask the general purpose LLM
to generate is based on the ${ATOMIC}^{20}_{20}$ knowledge graph and takes the form of a $(Event | Relation | Inference)$ triplet. 

<img width="891" alt="image" src="https://github.com/p0wp0wpanda/p0wp0wpanda.github.io/assets/43241208/61e54e15-d34c-4c61-a7ee-1ad629b3204f">
The knowledge graph's structure.

<br>
<br>

So the paper presents the following key findings:
  - Student models can out perform the teacher model after distillation
  - General purpose LLMs can (with some caveats) outperform humans in high-quality, knowledge graph generation


Read the full paper [here](https://arxiv.org/pdf/2110.07178.pdf)
