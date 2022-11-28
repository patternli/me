{% assign card=site.project-stories %}
<div class="card-group {{ card.settings.class | default: "grid-350" }}">
{% for c in card %}
    <div class="card {{ c.class }}">
        {% if c.feature %}
        <div class="card-image"><img src="{{ c.feature}}"></div>
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
        {% if c.short or c.meta %}
        <div class="card-body">
            {% if c.meta %}
            <p class="meta">{{ c.meta }}</p>
            {% endif %}
            {% if c.short %}
            {{ c.short | markdownify }}
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
