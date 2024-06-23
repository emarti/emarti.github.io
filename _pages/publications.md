---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: false
---

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

## Publications

{% assign total = site.publications.size %}
{% assign count = total %}
{% for post in site.publications reversed %}
  {{ count }}. **{{ post.title }}**  
   _{{ post.venue }}, {{ post.date | date: "%Y" }}_  
   {{ post.citation }}  
   [Link]({{ post.permalink }})

   {% assign count = count | minus: 1 %}
{% endfor %}



<!-- {% assign count = 1 %}
{% for post in site.publications %}
  {{ count }}. **{{ post.title }}**  
   _{{ post.venue }}, {{ post.date | date: "%Y" }}_  
   {{ post.citation }}  
   [Link]({{ post.permalink }})

   {% assign count = count | plus: 1 %}
{% endfor %} -->

<!-- ---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %} -->

