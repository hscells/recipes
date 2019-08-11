---
title: Home
---

<p>
All recipes are listed below in alphabetical order.
For a list of recipies ordered by the ingredients they contain, visit the <a href="ingredients/">ingredients page</a>.
This website is Open Source! For contributing, visit the project on <a href="https://github.com/hscells/recipes/">GitHub</a>.
</p>
<ul>
{%- assign recipes = site.recipe | sort:"title" -%}
{% for recipe in recipes %}
<li><a href="/recipes{{ recipe.url }}">{{ recipe.title }}</a></li>
{% endfor  %}
</ul>
