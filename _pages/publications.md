---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

{% if site.author.googlescholar %}
<p>You can also find my articles on <a href="{{ site.author.googlescholar }}">my Google Scholar profile</a>.</p>
{% endif %}

## Peer-reviewed publications

{% assign group = site.publications | where: "category", "published" | sort: "date" | reverse %}
{% for post in group %}
<h3>{{ post.title }}</h3>
<p>{{ post.authors }} &middot; <i>{{ post.venue }}</i>, {{ post.date | date: "%Y" }}</p>
{% if post.excerpt %}<p>{{ post.excerpt | markdownify }}</p>{% endif %}
{% if post.paperurl %}<p><a href="{{ post.paperurl }}">PDF</a>{% if post.link %} &middot; <a href="{{ post.link }}">Journal page</a>{% endif %}</p>{% endif %}
{% endfor %}

## Under review and in submission

{% assign group = site.publications | where: "category", "under-review" | sort: "date" | reverse %}
{% for post in group %}
<h3>{{ post.title }}</h3>
<p>{{ post.authors }} &middot; <i>{{ post.venue }}</i> &middot; {{ post.status }}</p>
{% if post.excerpt %}<p>{{ post.excerpt | markdownify }}</p>{% endif %}
{% if post.paperurl %}<p><a href="{{ post.paperurl }}">Preprint</a>{% if post.link %} &middot; <a href="{{ post.link }}">Journal page</a>{% endif %}</p>{% endif %}
{% endfor %}

## Working papers

{% assign group = site.publications | where: "category", "working" | sort: "date" | reverse %}
{% for post in group %}
<h3>{{ post.title }}</h3>
<p>{{ post.status }}</p>
{% if post.excerpt %}<p>{{ post.excerpt | markdownify }}</p>{% endif %}
{% endfor %}

---

Public writing and editing are listed on the [Writing](/writing/) page.
