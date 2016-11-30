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
  <li><a href="https://github.com/hnarayanan/shpotify">shpotify</a> for bringing spotify to the command line</li>
</ul>

# $ spotify play synthwave 
<iframe src="https://embed.spotify.com/?uri=spotify%3Auser%3Adj.jrkface%3Aplaylist%3A0HhLpehIcYpXYDCJ3CFeAN" width="256" height="80" frameborder="0" allowtransparency="true"></iframe>

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
      {% if project.demo %}
      <li>demo : <a href="{{ project.demo }}">{{ project.demo }}</a>,</li>
      {% endif %}
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
