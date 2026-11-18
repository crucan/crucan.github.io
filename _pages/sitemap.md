---
title: Sitemap
lang: ja
description: このサイトの全ページ一覧
---

<h2>ブログ</h2>
<ul>
{% for post in site.posts %}
  <li>
    <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
    <small>（{{ post.date | date: "%Y-%m-%d" }}）</small>
  </li>
{% endfor %}
</ul>

<h2>制作物</h2>
<ul>
{% for project in site.projects reversed %}
  <li>
    <a href="{{ project.url | prepend: site.baseurl }}">{{ project.title }}</a>
    {% if project.subtitle %}<small>（{{ project.subtitle }}）</small>{% endif %}
  </li>
{% endfor %}
</ul>

<h2>タグ</h2>
<ul>
{% for tag in site.tags %}
  <li>
    <a href="{{ site.baseurl }}/tag/{{ tag[0] | downcase }}">{{ tag[0] }}</a>
    <small>（{{ tag[1].size }}件）</small>
  </li>
{% endfor %}
</ul>

<h2>一覧・固定ページ</h2>
<ul>
  <li><a href="{{ site.baseurl }}/">ホーム</a></li>
  <li><a href="{{ site.baseurl }}/blog/">ブログ一覧</a></li>
  <li><a href="{{ site.baseurl }}/projects/">制作物一覧</a></li>
  <li><a href="{{ site.baseurl }}/about">About</a></li>
  <li><a href="{{ site.baseurl }}/contact">Contact</a></li>
</ul>
