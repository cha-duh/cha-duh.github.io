---
layout: default
---

# $ cat about.txt
{:id="about"}

track my development here

games, toys, algorithmic music generators, data analysis

my thanks to:
<ul>
  <li><a href="https://pages.github.com">github pages</a> for painless portfolio & infrequent blog maintenence</li>
  <li><a href="https://lampiaosec.github.io">lampiaosec</a> for the jekyll theme</li>
  <li><a href="https://csl.name/jp2a/">jp2a</a> for image-to-ascii conversion</li>
</ul>

# $ cat contact.txt
{:id="contact"}

<a href="https://github.com/cha-duh">github</a>

# $ cat projects.txt
{:id="projects"}

<ul>
{% for project in site.categories.projects %}
  <li>
    :: <a href="{{ project.link }}">{{ project.title }}</a> ::
    <ul><li>:: {{ project.description }} ::</li></ul>
  </li>
{% endfor %}
</ul>

# $ cat posts.txt
{:id="posts"}

<ul>
  {% for post in site.categories.posts %}
    <li>
      :: <a href="{{ post.url }}" title="{{ post.description }}">{{ post.title }}</a> ::
      <ul><li>:: date : {{post.date}} ::</li></ul>
    </li>
  {% endfor %}
</ul>

# $ cat articles.txt
{:id="articles"}

<ul>
{% for post in site.categories.articles %}
  <li>
    :: <a href="{{ post.url }}" title="{{ post.description }}">{{ post.title }}</a> ::
    <ul>
      <li>:: date : {{post.date}} :: </li>
    </ul>
  </li>
{% endfor %}
</ul>
