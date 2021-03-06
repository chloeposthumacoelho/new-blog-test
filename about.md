---
layout: dark
title: About
example: This is an example value.
---

I'm Chloe, an undergraduate computer science student. {{ site.title }} by {{ site.author.name }}.
{{ page.example }}

//{% include big-cat.html %}//

{% include profile-pic.png %}
![profile-pic](https://user-images.githubusercontent.com/96831510/175758093-771f102d-3436-4b16-ba0c-7b146995fd82.png)


## About About Pages

The About page is a common convention found on websites.
It is your opportunity to let us know all the details "about" your project:

- focus and topic area
- people involved
- code and projects used

## List of Animals

{% for animal in site.data.animals %}
- The {{ animal.name }} is a {{ animal.size }} animal.
{% endfor %}

## Large Animals are Better

{% for animal in site.data.animals %}
{% if animal.size == "large" %}- <strong style="color: {{ animal.color }};">{{ animal.name }}</strong>
{% else %}- <small>{{ animal.name }}</small>
{% endif %}
{% endfor %}

## List of Small Animals

{% assign small_animals = site.data.animals | where: "size", "small" %}
{% for animal in small_animals %}
- {{ animal.name | upcase }}
{% endfor %}
