---
layout: page
permalink: /publications/
title: publications
description:
nav: true
nav_order: 3
---

<!-- _pages/publications.md -->

<div class="publications-subsection-link"><a href="#journal-articles">journal articles <i class="fa-solid fa-turn-down"></i></a></div>
<div class="publications-subsection-link"><a href="#conference-presentations">conference presentations <i class="fa-solid fa-turn-down"></i></a></div>
<div class="publications-subsection-link"><a href="#additional-writings">additional writings <i class="fa-solid fa-turn-down"></i></a></div>

<!-- <div class="publications-subsection-link"><h4><a href="#articles-section">journal articles <i class="fa-solid fa-turn-down"></i></a></h4></div>
<div class="publications-subsection-link"><h4><a href="#presentations-section">conference presentations <i class="fa-solid fa-turn-down"></i></a></h4></div>
<div class="publications-subsection-link"><h4><a href="#writings-section">additional writings <i class="fa-solid fa-turn-down"></i></a></h4></div> -->

<br>

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<br>

<h2 id="journal-articles">journal articles</h2>

<div class="publications">

{% bibliography --file articles %}

</div>

<br>
<br>

<h2 id="conference-presentations">conference presentations</h2>

<div class="publications">

{% bibliography --file presentations %}

</div>

<br>
<br>

<h2 id="additional-writings">additional writings</h2>

<div class="publications">

{% bibliography --file writings %}

</div>