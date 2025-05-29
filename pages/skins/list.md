---
permalink: /skins/list.html
---
## List of all the skins
{: .no_toc}

{% include secondaryNavigation.liquid %}

**Skins on this Page:**

* TOC seed list
{:toc}

{% for skin in site.skins %}

### {{ skin.display_name }}

{% include linkToPage.liquid style=skin relation="before" %}

{% for diagram in site.diagrams %}

#### {{ diagram.display_name }} shown in {{ skin.display_name }}
{: .no_toc}

{% capture url %}{{ skin.url }}#{{ diagram.name }}{% endcapture %}

{% include figure.liquid style=skin diagram=diagram url=url %}

{% endfor %}

{% include linkToPage.liquid style=skin relation="after" %}

{% endfor %}
