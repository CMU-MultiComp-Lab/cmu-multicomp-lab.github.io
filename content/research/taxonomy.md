---
title: Taxonomy
col_class: gray editor
banner: /wp-content/uploads/2016/07/banner_library.jpg
heading: Research
sidebar: research
description: Taxonomy
---

<img alt="" class="aligncenter size-full wp-image-1429" height="211" src="/wp-content/uploads/2017/06/捕获-1.jpg" width="709"/>

The research field of Multimodal Machine Learning brings some unique challenges for computational researchers given the heterogeneity of the data. Learning from multimodal sources offers the possibility of capturing correspondences between modalities and gaining an in-depth understanding of natural phenomena. In our work, we identify and explore five core technical challenges (and related sub-challenges) surrounding multimodal machine learning. They are central to the multimodal setting and need to be tackled to progress the field. Our taxonomy goes beyond the typical early and late fusion split, and consists of the five following challenges:

**Representation:**A first fundamental challenge is learning how to represent and summarize multimodal data in a way that exploits the complementarity and redundancy of multiple modalities. The heterogeneity of multimodal data makes it challenging to construct such representations. For example, language is often symbolic while audio and visual modalities will be represented as signals.

**Translation:**A second challenge addresses how to translate (map) data from one modality to another. Not only is the data heterogeneous, but the relationship between modalities is often open-ended or subjective. For example, there exist some correct ways to describe an image, and one perfect translation may not exist.

**Alignment:**A third challenge is to identify the direct relations between (sub)elements from two or more different modalities. For example, we may want to align the steps in a recipe to a video showing the dish being made. To tackle this challenge we need to measure the similarity between different modalities and deal with possible long-range dependencies and ambiguities.

**Fusion:**A fourth challenge is to join information from two or more modalities to perform a prediction. For example, for audio-visual speech recognition, the visual description of the lip motion is fused with the speech signal to predict spoken words. The information coming from different modalities may have different predictive power and noise topology, with possibly missing data in at least one of the modalities.

**Co-learning:**The fifth challenge is to transfer knowledge between modalities, their representation, and their predictive models. This area of work is exemplified by algorithms of co-training, conceptual grounding, and zero shot learning. Co-learning explores how knowledge learning from one modality can help a computational model trained on a different modality. This challenge is particularly relevant when one of the modalities has limited resources (e.g., annotated data).
