{% assign card=include.content %}
<div class="{{ card.settings.class }}">
{% for c in card.list %}
    <div class="card {{ c.class }}">
        {% if c.image %}
        <div class="card-image"><img src="{{ c.image}}"></div>
        {% endif %}
        {% if c.title or c.flag %}
        <div class="card-header">
            {% if c.title %}
            <h3>{{ c.title }}</h3>
            {% endif %}
            {% if c.flag %}
            <div class="card-flag">super</div>
            {% endif %}
        </div>
        {% endif %}
        {% if c.body or c.meta %}
        <div class="body">
            {% if c.meta %}
            <p class="meta">{{ c.meta }}</p>
            {% endif %}
            {% if c.body %}
            <p>{{ c.body }}</p>
            {% endif %}
        </div>
        {% endif %}
        <div class="card-footer">
            <a href="/">A link to somewhere</a>
        </div>
    </div>
    {% endfor %}
</div>
