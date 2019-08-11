---
title: Recipes by ingredient
---

<p>All recipes ordered by the ingredients they contain.</p>
{%- assign ingredients = site.recipe | map: 'ingredients' | join: ','  | split: ',' | uniq | sort -%}
{%- for ingredient in ingredients -%}
<b>{{ingredient}}</b>
<ul>
    {%- for recipe in site.recipe -%}
    {%- assign found = false -%}
    {%- for i in recipe.ingredients -%}
        {%- if i == ingredient -%}
            {%- assign found = true -%}
        {%- endif -%}
    {%- endfor -%}    
    {%- if found -%}
    <li><a href="/recipes{{recipe.url}}">{{recipe.title}}</a></li>
    {%- endif -%}
    {%- endfor -%}
</ul>    
{%- endfor -%}
