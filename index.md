---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: page
---

<ul>
  {% for post in site.posts %}
    <li>
      <article>
        <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
        <small>{{ post.date }}</smalL>
        <p>{{ post.excerpt }}</p>
      </article>
    </li>
  {% endfor %}
</ul>
