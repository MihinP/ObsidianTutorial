---
Status: TOREAD
paperstatus: <em>#paper</em>
---
# {{title}}
#### {{authors}}
___
**Title**:: {{title}}
**Journal/Book**:: 
**Publisher**:: {{publisher}}{{publicationTitle}}
**FirstAuthor**:: {{creators[0].firstName}} {{creators[0].lastName}}
**Date**:: {{date.year()}}
**Link**:: [Zotero Link]({{select}})
**DOI**:: https://doi.org/{{DOI}}
**CiteKey**:: @{{citekey}}
**Tags**:: 
___
>[!abstract]
>{{abstractNote}}


>[!summary] 
>**Synthesis**:: 

___
{% macro heading(color) -%}
{%- if color == "#5fb236" -%}
Main ideas and conclusions
{%- endif -%}
{%- if color == "#2ea8e5" -%}
Results
{%- endif -%}
{%- if color == "#ffd400" -%}
Methodology
{%- endif -%}
{%- if color == "#a28ae5" -%}
Definitions and concepts
{%- endif -%}
{%- if color == "#ff6666" -%}
Weaknesses and caveats
{%- endif -%}
{%- if color == "#f19837" -%}
Instruments and Technology
{%- endif -%}
{%- if color == "#aaaaaa" -%}
Hypothesis
{%- endif -%}
{%- endmacro -%}

{% macro calloutCharacter(color) -%}
{%- if color == "#5fb236" -%}
$
{%- endif -%}
{%- if color == "#2ea8e5" -%}
@
{%- endif -%}
{%- if color == "#ffd400" -%}
&
{%- endif -%}
{%- if color == "#a28ae5" -%}
~
{%- endif -%}
{%- if color == "#ff6666" -%}
!
{%- endif -%}
{%- if color == "#e56eee" -%}
€
{%- endif -%}
{%- if color == "#f19837" -%}
?
{%- endif -%}
{%- if color == "#aaaaaa" -%}
%
{%- endif -%}
{%- endmacro -%}

## Reading notes
{% for color, annotations in annotations | groupby("color") -%}
### {{heading(color)}}
{% for a in annotations -%}
{% if a.annotatedText %}
- {{calloutCharacter(a.color)}} {{a.annotatedText}}
{% endif %}
{% if a.comment %}
- {{calloutCharacter(a.color)}} {{a.comment}}
{% endif %}
{% if a.imageRelativePath %}
![[{{a.imageRelativePath}}]]
{% endif %}
{% endfor %}
{% endfor %}
