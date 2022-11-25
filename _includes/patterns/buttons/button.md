{% for link in include.content %}
<a class="{{link.class}}" href="{{ link.link }}">{{ link.text }}</a>
{% endfor %}
