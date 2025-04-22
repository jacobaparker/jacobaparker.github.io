---
layout: page
title: Modeling Pupil Responses
description: 
img: assets/img/pupil-modeling.png
importance: 1
category: previous work
related_publications: true
---

This is the project I worked on as an undergraduate research assistant in the [Carrasco lab](https://wp.nyu.edu/carrascolab/). The following is adapted from a [Twitter thread](https://x.com/jake_a_parker/status/1282730895624085506) that was originally posted on July 13, 2020.

<br>

## Summary

***

Pupil size is an indicator of various cognitive processes, making it potentially useful for assessing task-related processing dynamics. [Rachel Denison](https://sites.bu.edu/denisonlab/), [Marisa Carrasco](https://wp.nyu.edu/carrascolab/), and I developed a model that allows one to evaluate these dynamics by linking pupil responses to trial events {% cite denisonModelingPupilResponses2020 %}.

{% include centered_figure.liquid
   src="/assets/img/publication_preview/PRET.gif"
   alt="Animation of the pupil resonse model fitting procedure"
   caption="Pupil responses to individual events (colored curves) being fit to an artificial pupil area time series."
   width="70%"
   zoomable=true
%}

<br>

We created an open-source Matlab toolbox (Pupil Response Estimation Toolbox - PRET) that allows one to easily model pupil responses:
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
    {% include repository/repo.liquid repository='jacobaparker/PRET' %}
</div>

<br>

## More Details

***

The dynamics of pupil dilation are sluggish, taking ~1 sec to fully dilate in response to an internal cognitive signal (tmax below - units in ms). When many such signals occur within 1-2 secs, it is difficult to attribute changes in pupil size to any single signal.

{% include centered_figure.liquid
   src="/assets/img/prf.png"
   alt="Pupil response function"
   width="50%"
   zoomable=true
%}

<br>

This challenge has been previously addressed using a modeling paradigm that assumes that trial events elicit internal cognitive signals that drive pupil dilation responses, and that the measured pupil size time series is the linear combination of these pupil responses. The pupil response to an instantaneous cognitive signal is given by the pupil response function (A). Convolution of this function with the cognitive signals presumed to be associated with each trial event (B) gives the estimated pupil responses (C). 

{% include centered_figure.liquid
   src="/assets/img/pupil-modeling-theory.png"
   alt="Figure with subplots showing how pupil responses to individual events are modeled when the events occur close together in time"
   width="40%"
   zoomable=true
%}

<br>

Estimating model parameters (i.e. cognitive signal amplitudes) by fitting to pupil size data recorded during task completion allows one to make inferences about the cognitive signals related to each trial event. This approach is very similar to the general linear model framework used in many task fMRI analyses, where the hemodynamic response function is analogous to the pupil response function.

Despite the promising utility of this approach to pupil modeling, no standard procedure exists for implementing it. Various combinations of model elements and parameters have been tried, with cognitive signal amplitude being the only commonality. We conducted a factorial model comparison to determine what model elements/parameters should be included by fitting all possible models (24) to pupil size data from two temporal attention experiments. The model with the lowest BIC for the most observers was our criteria.

This comparison suggested that pupil dynamics are highly variable across individuals, and that modeling this inter-observer variability is imperative. Model fits improved significantly when the pupil response function (tmax parameter) was fit for each observer.

{% include centered_figure.liquid
   src="/assets/img/pupil-model-comparison.png"
   alt="A plot comparing how well 24 different pupil response models fit individual subjects"
   width="90%"
   zoomable=true
%}

<br>

In fact, model parameters generally tended to be more consistent across task conditions within individuals than across individuals within task conditions. This further underscores the need to account for individual variability.

{% include centered_figure.liquid
   src="/assets/img/pupil-individual-differences.png"
   alt="A plot showing parameter fits for all subjects and conditions"
   width="90%"
   zoomable=true
%}

<br>

We also found that cognitive signals should not be assumed to occur simultaneously with the associated trial event. When we included a time shift parameter (latency) for each cognitive signal in the model, the fit improved significantly (see above). Such a time shift was found when fitting the winning model to our data. Specifically, we found that pupil dilation anticipated predictable trial events – see precue and T1 in panel B.

{% include centered_figure.liquid
   src="/assets/img/pupil-parameter-estimates.png"
   alt="Group mean parameter estimates for the winning model"
   width="50%"
   zoomable=true
%}

<br>

Finally, we found that event-related pupil dilation amplitudes were larger for all trial events in the discrimination task as opposed to the estimation task – see panel A directly above (experimental design between these two tasks was identical apart from report type).

For more information about the experimental procedure, parameter estimation, model validation, reliability of parameter estimates, and more, check out the paper, [Modeling pupil responses to rapid sequential events.](https://link.springer.com/article/10.3758/s13428-020-01368-6)

<br>