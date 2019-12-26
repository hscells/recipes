---
title: Home
---

<p>
Welcome to my website of vegetarian recipes (most are also vegan). 
I cook cook most of these on a regular basis, usually when I get home in the evening.
For this reason, they are generally simple, fast, and affordable.
I like cooking (and eating), and I like to think that all of these recipes are nutritious and yummy.
</p>
<p>
All recipes are listed below in alphabetical order.
For a list of recipies ordered by the ingredients they contain, visit the <a href="ingredients/">ingredients page</a>.
This website, including the recipes, is Open Source! For contributing, visit the project on <a href="https://github.com/hscells/recipes/">GitHub</a>.
</p>
<ul>
{%- assign recipes = site.recipe | sort:"title" -%}
{% for recipe in recipes %}
<li><a href="/recipes{{ recipe.url }}">{{ recipe.title }}</a></li>
{% endfor  %}
</ul>
