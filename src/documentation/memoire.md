---
layout: layouts/base.html
title: /Mémoire
tags: documentation
---

<ul>
{%- for memoire in collections.memoire -%}
<li> <a href="{{memoire.url}}">{{memoire.data.title}}</a>
{%- endfor -%}
</ul>