---
title: "The Neurosymbolic concept learner"
collection: talks
permalink: /talks/ns-learner
date: 2023-06-11
---

The neurosymbolic concept learner is a very interesting model that attempts to learn concepts by jointly understanding vision and language
The model is designed to tackle question from a Visual Question Answer data set that usually consists of an image and a question answer pair.

<img width="891" alt="image" src="https://github.com/p0wp0wpanda/p0wp0wpanda.github.io/assets/43241208/61e54e15-d34c-4c61-a7ee-1ad629b3204f">


The model has 3 major parts:

The perception module: Takes the input image and generations proposals and extract visual representations for each of the proposal. 

The semantic parsing module: Translate a natural language question into an executable program with a hierarchy of primitive operations.

The quasi-symbolic reasoning module: Given the recovered program, a symbolic program executor executes the program and derives the answer based on the object-based visual representation and the concept embeddings

Check out the paper [here](https://arxiv.org/abs/1904.12584)
