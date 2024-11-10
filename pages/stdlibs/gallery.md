---
permalink: /stdlibs/gallery.html
---
## Stdlibs Gallery
{: .no_toc}

{% include secondaryNavigation.html %}

**Stdlibs on this Page:**

* TOC seed list
{:toc}

{% for stdlib in site.stdlibs %}

### {{ stdlib.display_name }}

Go to the page for the [{{ stdlib.display_name }}]({{ stdlib.url | relative_url }})

<div class="image-gallery">

{% for theme in site.themes %}

{% capture url %}{{ stdlib.url }}#{{ theme.name }}{% endcapture %}
{% capture caption %}{{ theme.display_name }}{% endcapture %}

{% include figure.html theme=theme diagram=stdlib url=url caption=caption %}

{% endfor %}

</div>

Go to the page for the [{{ stdlib.display_name }}]({{ stdlib.url | relative_url }})

{% endfor %}