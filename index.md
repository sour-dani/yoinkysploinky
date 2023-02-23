---
layout:     none
---

<html>
    {% include base.html %}
    <body>
        {% assign month = site.time | date: '%-m' %}
        {% assign day = site.time | date: '%-d' %}
        {% assign video = "false" %}
        {% assign gif = "yoinky" %}
        {% if month == "2" %}
            {% if day == "1" %}
                {% assign gif = "kittysploink" %}
            {% endif %}
        {% elsif month == "3" %}
            {% if day == "29" %}
                {% assign video = "true" %}
                <video autoplay loop muted controls>
                    <source src="img/cowpokeyoink.mp4" type="video/mp4">
                </video>
            {% endif %}
        {% elsif month == "5" %}
            {% if day == "25" %}
                {% assign gif = "dayoink" %}
            {% endif %}
        {% elsif month == "6" %}
            {% if day == "9" %}
                {% assign gif = "that-yoink" %}
            {% endif %}
        {% elsif month == "8" %}
            {% if day == "18" %}
                {% assign gif = "jermayoink1" %}
            {% elsif day == "19" %}
                {% assign gif = "jermayoink2" %}
            {% endif %}
        {% elsif month == "10" %}
            {% if day == "19" %}
                {% assign gif = "wheelyoink" %}
            {% endif %}
        {% endif %}
        {% if video == "false" %}
            <img id="sploinky_gif" src="img/{{gif}}.gif">
        {% endif %}
    </body>