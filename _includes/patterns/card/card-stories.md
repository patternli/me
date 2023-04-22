{% assign card=site.project-stories %}
<div class="card-group {{ card.settings.class | default: 'grid-350' }}">
{% for c in card limit: include.limit %}
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
        <div class="card-foot">
            <a href="{{ c.url }}" class="btn">Read about this project</a>
        </div>
    </div>
    {% endfor %}
</div>
