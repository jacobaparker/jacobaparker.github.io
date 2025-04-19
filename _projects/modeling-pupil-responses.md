---
layout: page
title: Modeling Pupil Responses
description: My undergraduate work
img: assets/img/pupil-modeling.png
importance: 1
category: previous work
related_publications: true
---

## Summary

Pupil size is an indicator of various cognitive processes, making it potentially useful for assessing task-related processing dynamics. [Rachel Denison](https://sites.bu.edu/denisonlab/), [Marisa Carrasco](https://wp.nyu.edu/carrascolab/), and I developed a model that allows one to evaluate these dynamics by linking pupil responses to trial events {% cite denisonModelingPupilResponses2020 %}.

<img align="middle" src="/assets/img/publication_preview/PRET.gif" alt="Visualization of fitting the pupil response model to artificial data" style="width:512px;">

<!-- ![Visualization of fitting the pupil response model to artificial data](/assets/img/publication_preview/PRET.gif) -->

We created an open-source Matlab toolbox (Pupil Response Estimation Toolbox - PRET) that allows one to easily model pupil responses:
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
    {% include repository/repo.liquid repository='jacobaparker/PRET' %}
</div>

<br>

## More Details

The dynamics of pupil dilation are sluggish, taking ~1 sec to fully dilate in response to an internal cognitive signal (tmax below - units in ms). When many such signals occur within 1-2 secs, it is difficult to attribute changes in pupil size to any single signal.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Pupil size is an indicator of various cognitive processes, making it potentially useful for assessing task-related processing dynamics<a href="https://twitter.com/rndenison?ref_src=twsrc%5Etfw">@rndenison</a>, Marisa Carrasco, and I developed a model that allows one to evaluate these dynamics by linking pupil responses to trial events<br><br>1/N <a href="https://t.co/giVP9uMAbf">pic.twitter.com/giVP9uMAbf</a></p>&mdash; Jake Parker (@jake_a_parker) <a href="https://twitter.com/jake_a_parker/status/1282730895624085506?ref_src=twsrc%5Etfw">July 13, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
    {% include repository/repo.liquid repository='jacobaparker/PRET' %}
</div>