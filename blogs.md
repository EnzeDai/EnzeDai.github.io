---
layout: homepage
permalink: /blogs/
---

## Blogs

Personal notes, diaries, and technical writings.

{% assign posts = site.posts %}

{% if posts.size > 0 %}
{% for post in posts %}
### [{{ post.title }}]({{ post.url | relative_url }})

<small>{{ post.date | date: "%Y-%m-%d" }}</small>

{% if post.excerpt %}
{{ post.excerpt }}
{% endif %}

{% endfor %}
{% else %}
No posts yet.
{% endif %}

---

[← Back to homepage]({{ "/" | relative_url }})
