---
layout: page
title: Today I Learned
permalink: /til/
---
<h1 align="center">Today I Learned</h1>
<h4 align="center">Inspired by Phan An's
<a href="https://til.phanan.net/" target="_blank">TIL </a> website </h4>
{% assign tils = site.tils | sort: 'date' | reverse %}
{% for til in tils %}
  {{ til.content }}
  <hr>
{% endfor %}
