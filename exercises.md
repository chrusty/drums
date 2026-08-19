---
layout: home
# title: Exercises
---
<h1>Exercises</h1>

<ul>
    {% for exercise in site.exercises %}
    <li>
        <h2>
            <a href="{{site.baseurl}}{{ exercise.url }}">
                {{ exercise.name }}
            </a>
            ({{ exercise.type }})
            {% if exercise.tags.size > 0 %}
            {% for tag in exercise.tags %}[{{tag}}] {% endfor %}
            {% endif %}
        </h2>
    </li>
    {% endfor %}
</ul>