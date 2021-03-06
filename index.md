---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
title: Home
layout: slideshow
extra_css:
- slideshow
js_file:
- slideshow
---
<div class="slideshow-container">
    {% for image in site.static_files %}
        {% if image.path contains 'images/products' %}
            <div class="mySlides fade">
                <img src="{{ site.base_url }}{{ image.path }}" class="slideshow-content" width="100%" height="100%"/>
            </div>
        {% endif %}
    {% endfor %}
</div>