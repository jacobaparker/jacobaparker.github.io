---
layout: page
permalink: /publications/
title: publications
description: Click on a section name to jump to it.
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<h3><a href="#articles-section">journal articles</a></h3>
<h3><a href="#presentations-section">conference presentations</a></h3>
<h3><a href="#writings-section">additional writings</a></h3>

<br>

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<br>

<h2 id="articles-section">journal articles</h2>

<div class="publications">

{% bibliography --file articles %}

</div>

<br>
<br>

<h2 id="presentations-section">conference presentations</h2>

<div class="publications">

{% bibliography --file presentations %}

</div>

<br>
<br>

<h2 id="writings-section">additional writings</h2>

<div class="publications">

{% bibliography --file writings %}

</div>