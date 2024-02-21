---
layout: layouts/base.html
<!-- css: assets/css/style.css -->
---

<ul>
{%- for documentation in collections.documentation -%}
<li> <a href="{{documentation.url}}">{{documentation.data.title}}</a>
{%- endfor -%}
</ul>