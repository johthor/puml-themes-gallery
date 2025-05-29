---
permalink: /skins/gallery.html
---
## Skins Gallery
{: .no_toc}

{% include secondaryNavigation.liquid %}

**Skins on this Page:**

* TOC seed list
{:toc}

{% for skin in site.skins %}

### {{ skin.display_name }}

{% include linkToPage.liquid style=skin relation="before" %}

<div class ="image-gallery">

{% for diagram in site.diagrams %}

{% capture url %}{{ skin.url }}#{{ diagram.name }}{% endcapture %}
{% capture caption %}{{ diagram.display_name }}{% endcapture %}

{% include figure.liquid style=skin diagram=diagram url=url caption=caption %}

{% endfor %}

</div>

{% include linkToPage.liquid style=skin relation="after" %}

{% endfor %}
