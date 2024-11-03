---
permalink: /diagrams/list.html
---
## List of all the Diagrams
{: .no_toc}

{% include secondaryNavigation.html %}

**Diagrams on this Page:**

* TOC seed list
{:toc}

{% for diagram in site.diagrams %}

### {{ diagram.display_name }}

Go to the page for the [{{ diagram.display_name }}]({{ diagram.url }})

{% for theme in site.themes %}

#### {{ diagram.display_name }} shown in {{ theme.display_name }}
{: .no_toc}

{% capture url %}{{ diagram.url }}#{{ theme.name }}{% endcapture %}

{% include figure.html theme=theme diagram=diagram url=url %}

{% endfor %}

Go to the page for the [{{ diagram.display_name }}]({{ diagram.url }})

{% endfor %}