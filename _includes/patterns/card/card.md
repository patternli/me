{% assign card=include.content %}
<div class="card-group {{ card.settings.class }}">
{% for c in card.list %}
    <div class="card {{ c.class }}">
        {% if c.image %}
        <div class="card-image"><img src="{{ c.image}}"></div>
        {% endif %}
        {% if c.title or c.flag %}
        <div class="card-head">
            {% if c.title %}
            <h3>{{ c.title }}</h3>
            {% endif %}
            {% if c.flag %}
            <div class="card-flag">{{ c.flag }}</div>
            {% endif %}
        </div>
        {% endif %}
        {% if c.body or c.meta %}
        <div class="card-body">
            {% if c.meta %}
            <p class="meta">{{ c.meta }}</p>
            {% endif %}
            {% if c.body %}
            <p>{{ c.body }}</p>
            {% endif %}
        </div>
        {% endif %}
        {% if c.links %}
        <div class="card-foot">
            {% include patterns/buttons/button.md content=c.links %}
        </div>
        {% endif %}
    </div>
    {% endfor %}
</div>
