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

# $ cat projects.json
{:id="projects"}

<ul>
{% for project in site.categories.projects %}
  <li>{
    <ul>
      <li>name : {{ project.title }},</li>
      <li>link : <a href="{{ project.link }}">{{ project.link }}</a>,</li>
      <li>desc : {{ project.description }}</li>
    </ul>
  }</li>
{% endfor %}
</ul>

# $ cat posts.json
{:id="posts"}

<ul>
  {% for post in site.categories.posts %}
    <li>{
      <ul>
        <li>name : {{ post.title}},</li> 
        <li>link : <a href="{{ post.url }}">{{ post.url }},</a></li>
        <li>date : {{ post.date }},</li>
        <li>keys : "{{ post.keywords }}",</li>
        <li>desc : {{ post.description }}</li>
      </ul>
    }</li>
  {% endfor %}
</ul>

# $ cat articles.json
{:id="articles"}

<ul>
  {% for post in site.categories.articles %}
    <li>{
      <ul>
        <li>name : {{ post.title}},</li> 
        <li>link : <a href="{{ post.url }}">{{ post.url }}</a>,</li>
        <li>date : {{ post.date }},</li>
        <li>keys : "{{ post.keywords }}",</li>
        <li>desc : {{ post.description }}</li>
      </ul>
    }</li>
  {% endfor %}
</ul>
