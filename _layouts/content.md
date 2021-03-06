---

---

<!DOCTYPE html>
<html lang="id">
    <head>
        <title> {{ site.title }} | {{ page.title }} </title>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta property="og:locale" content="id_ID">
        <meta property="og:type" content="website">
        <meta property="og:title" content="{{ site.title }} | {{ page.title }}">
        <meta name="description" content="{{ site.description | truncate: 160 }}">
        <meta property="og:description" content="{{ site.description | truncate: 160 }}">
        <meta property="og:site.name" content="{{ site.title }}">
        <link rel="shortcut icon" type="image/x-icon" href="{{ site.base_url }}/favicon.ico?">
        <link rel="stylesheet" type="text/css" href="{{ site.base_url }}/assets/css/main.css">
        <link rel="stylesheet" type="text/css" href="{{ site.base_url }}/assets/css/content.css">
        {% if page.extra_css %}
			{% for stylesheet in page.extra_css %}
				<link rel="stylesheet" type="text/css" href="{{ site.base_url }}/assets/css/{{ stylesheet }}.css">
			{% endfor %}
		{% endif %}
    </head>
    <body>
        <div class="outer-container">
            <div class="container">
                {% include header.md %}
                <div class="content">
                    {{ content }}
                </div>
                {% include footer.md %}
                </div>
            </div>
        </div>
        <script type="text/javascript" src="{{ site.base_url }}/assets/js/dropdown-navbar.js"></script>
        <script type="text/javascript" src="{{ site.base_url }}/assets/js/responsive-navbar.js"></script>
        {% if page.js_file %}
            {% for js in page.js_file %}
                <script type="text/javascript" src="{{ site.base_url }}/assets/js/{{ js }}.js"></script>
            {% endfor %}
        {% endif %}
    </body>
</html>