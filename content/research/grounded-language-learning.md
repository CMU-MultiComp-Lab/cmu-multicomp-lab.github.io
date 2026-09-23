---
title: Grounded Language Learning
col_class: gray editor
banner: /wp-content/uploads/2016/07/banner_library.jpg
heading: Research
sidebar: research
description: Grounded Language Learning
---

<img alt="" class="aligncenter wp-image-1520" height="275" src="/wp-content/uploads/2021/03/gll-3.png" width="341"/>
One of the long-standing goals of artificial intelligence research is enabling humans to communicate with machines using natural language interfaces. The fundamental problem of achieving this is grounded language learning. Grounded language learning is the task of learning the meaning of natural language units (e.g., utterances, phrases, or words) by leveraging the sensory data (e.g., an image). Grounded language learning is a challenging task from a computational perspective due to the inherent ambiguity in natural language and the imperfect sensory data.

We study grounded language learning in the context of learning an interpretable model for referring expressions, i.e., localizing a visual object described by a natural language expression. We propose GroundNet, a dynamic neural architecture for localizing objects mentioned in a referring expression for an image.  Our model takes advantage of natural language compositionality to improve interpretability but can maintain high predictive accuracy. Critically, our approach relies on a syntactic analysis of the input referring expression to shape the computation graph. We find that this form of inductive bias helpfully constrains the learned model’s interpretation, but proves not to be overly restrictive. An important intermediate step for grounding referring expressions is the localization of supporting object mentions. Our experiments on the GoogleRef dataset show that GroundNet successfully identifies intermediate supporting objects while maintaining comparable performance to state-of-the-art approaches.
