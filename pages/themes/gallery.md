---
permalink: /themes/gallery.html
---
## Themes Gallery
{: .no_toc}

{% include secondaryNavigation.html %}

**Themes on this Page:**

* TOC seed list
{:toc}

{% for theme in site.themes %}

### {{ theme.display_name }}

Go to the page for the [{{ theme.display_name }}]({{ theme.url | relative_url }}).

<div class ="image-gallery">

{% for diagram in site.diagrams %}

{% capture url %}{{ theme.url | relative_url }}#{{ diagram.name }}{% endcapture %}
{% capture caption %}{{ diagram.display_name }}{% endcapture %}

{% include figure.html theme=theme diagram=diagram url=url caption=caption %}

{% endfor %}

</div>

Go to the page for the [{{ theme.display_name }}]({{ theme.url | relative_url }}).

{% endfor %}
