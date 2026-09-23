---
title: Multimodal Representation
col_class: gray editor
banner: /wp-content/uploads/2016/07/banner_library.jpg
heading: Research
sidebar: research
description: One of the greatest challenges of multimodal data is to summarize the information from multiple modalities (or views) in a way that complementary information is used as a conglomerate while filtering out the redundant parts of the modalities. Due to the heterogeneity of the data, some challenges naturally spring up including different kinds of noise,
---

<img alt="" class="aligncenter size-full wp-image-1431" height="298" src="/wp-content/uploads/2017/06/捕获1.jpg" width="676"/>

One of the greatest challenges of multimodal data is to summarize the information from multiple modalities (or views) in a way that complementary information is used as a conglomerate while filtering out the redundant parts of the modalities. Due to the heterogeneity of the data, some challenges naturally spring up including different kinds of noise, alignment of modalities (or views) and, techniques to handle missing data. We study multimodal representations using two broad approaches, Joint and Coordinated.

Joint Representations involve projecting all the modalities to a common space while preserving information from the given modalities. Data from all modalities is required at training and inference time which can potentially make dealing with missing data hard. In our study, we propose a recurrent model which can fuse different views of a modality at each time-step and finally use the joint representation to complete the task at hand (like classification, regression, etc.).

Coordinated Representations involve projecting all the modalities to their space, but those spaces are coordinated using a constraint. This kind of an approach is more useful for modalities which are fundamentally very different and might not work well in a joint space. Due to the variety of modalities in nature, Coordinated Representations have a huge advantage over Joint Representations which gives us reason to believe that the coordination using constraints is the way to go in the field of multimodal representation.
