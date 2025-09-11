---
permalink: /
title: "Overview"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

Welcome to my personal site! Here you'll find my latest work, blog posts, CV, portfolio, and more.

## Recent Activity

### Recent Blog Posts

{% assign recent_posts = site.posts | where_exp: "post", "post.date <= site.time" | sort: "date" | reverse | slice: 0,3 %}

<ul>
  {% for post in recent_posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> <span style="color: #888;">({{ post.date | date: "%b %d, %Y" }})</span>
    </li>
  {% endfor %}
</ul>

### Recent LinkedIn Post

<a href="https://www.linkedin.com/in/han-lin-chen/recent-activity/all/" target="_blank">See my latest on LinkedIn</a>

## About This Site

This site is powered by Jekyll and GitHub Pages. It features:

- Data-driven content (CV, publications, talks, teaching, portfolio)
- Blog posts and technical writing
- Downloadable resume ([PDF](/files/LeoChenResume.pdf))
- Source code and configuration on [GitHub](https://github.com/hanlinchentw/hanlinchentw.github.io)

Feel free to explore, connect, or reach out!

---

_Last updated: {{ site.time | date: "%B %d, %Y" }}_
