---
title: PATS (Pose, Audio, Transcript, Style) Dataset
col_class: gray editor
banner: /wp-content/uploads/2016/07/banner_library.jpg
heading: Resources
sidebar: resources
description: PATS was collected to study correlation of co-speech gestures with audio and text signals. The dataset consists of a diverse and large amount of aligned pose, audio and transcripts. With this dataset, we hope to provide a benchmark which would help develop technologies for virtual agents which generate natural and relevant gestures. The Dataset
---

<img class="aligncenter wp-image-1912" src="/wp-content/uploads/2020/12/pats_overview.png"/>

PATS was collected to study correlation of co-speech gestures with audio and text signals. The dataset consists of a diverse and large amount of aligned pose, audio and transcripts. With this dataset, we hope to provide a benchmark which would help develop technologies for virtual agents which generate natural and relevant gestures.

The Dataset Contains:

- Transcribed **Pose** data with aligned **Audio** and **Transcriptions**
  - 25 Speakers with different **Styles**
  - Includes 10 speakers from [Ginosar, et al. (CVPR 2019)](https://people.eecs.berkeley.edu/~shiry/projects/speech2gesture/index.html)
  - 15 talk show hosts, 5 lecturers, 3 YouTubers, and 2 televangelists
- 251 hours of data
  - Around ~ 84000 intervals
  - Mean: 10.7s per interval
  - Standard Deviation: 13.5s per interval

The dataset is available to download here: [**PATS Dataset Website**](http://chahuja.com/pats/).

Three modalities -i.e. Pose, Audio, Transcriptions- in many Styles available in the PATS dataset present a unique opportunity for the following tasks:

<img alt="" class="aligncenter wp-image-1919" src="/wp-content/uploads/2020/12/pats_tasks.png"/>

The following features are available:

<img alt="" class="aligncenter wp-image-1915" src="/wp-content/uploads/2020/12/pats_features.png"/>

The speakers in PATS have diverse lexical content in their transcripts along with diverse gestures. The following graphs will help you navigate through the speakers in the dataset, should you want to work with specific speakers with a different gesture and/or lexical diversities.

Fig 1 shows speakers clustered hierarchically based on the content of their transcripts and Fig 2 shows each speaker’s position on a lexical diversity vs spatial extent plot.

As shown in Fig. 1, speakers in the same domain (i.e. TV Show Hosts) share similar language, as demonstrated in the clusters. Furthermore, in Fig. 2, we can see that TV show speakers are generally more expressive with their hands and and words while Televangelists are less so. Speakers on the top right corner of Fig 2, are more challenging to model in the task of gesture generation as they have a greater diversity of vocabulary as well as gestures.

<img alt="" class="aligncenter wp-image-1916" src="/wp-content/uploads/2020/12/pats_graphs.png"/>
