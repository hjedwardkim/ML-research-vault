---
title: {{title}}
authors: {{authors}}
year: {{year}}
status: "first pass"
created: 
tags: {% for tag in tags %}{{tag.tag}} {% endfor %}
zotero: {{select}}
paperUrl: {{url}}
codeUrl: 
type: paper
---

## Zotero Annotations
{% if annotations %}
{% for annotation in annotations | sort(attribute="page") %}
{% if annotation.type == "highlight" %}
> {{annotation.annotatedText}}
{% if annotation.comment %}
> {{annotation.comment}}
{% endif %}
{% endif %}

{% if annotation.type == "note" %}
📝 **Note**
> {{annotation.comment}}
{% endif %}

{% if annotation.type == "image" %}
![[{{annotation.imageRelativePath}}]]
{% if annotation.comment %}
> {{annotation.comment}}
{% endif %}
{% endif %}

{% if annotation.type == "text" %}
✍️ **Text Insert**
> {{annotation.text}}
{% if annotation.comment %}
> {{annotation.comment}}
{% endif %}
{% endif %}

{% endfor %}
{% endif %}
## Other Annotations


## Key Points

## Methods

## Results

## Critical Insights

## Related Papers
