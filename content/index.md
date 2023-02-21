---
slogan: CONCEPTUAL ART - FASHION
intro: PHOTOART
banner: /img/photographerart.webp
start: CREATIVEBYDRE PHOTO ART GALLERY
cover: /img/photographer.webp
gallery: /img/beautycolourphotography.webp
gallerylink: /gallery/
coverfooter: /img/streetphotoart-human.webp
layout: layouts/art.njk
eleventyNavigation:
  key: Home
  order: 1
numberOfLatestPostsToShow: 4
---
<div class="col-md-12 mt-5 p-3 text-center">
<h3><strong><a href="{{metadata.url}}">PHOTO BLOG UPDATE</a></strong></h3>
<p>Our photo art services and blog update</p>
</div>
{% set postsCount = collections.posts | length %}
{% set latestPostsCount = postsCount | min(numberOfLatestPostsToShow) %}
{% set postslist = collections.posts | head(-1 * numberOfLatestPostsToShow) %}
{% set postslistCounter = postsCount %}
{% include "postslist.njk" %}
<div class="col-md-12 p-3 text-center">
{% set morePosts = postsCount - numberOfLatestPostsToShow %}
{% if morePosts > 0 %}
<p><a class="btn btn-light" href="/blog/">Explore all Post</a></p>
{% endif %}
</div>
{# List every content page in the project #}
{#
<ul>
{%- for entry in collections.all %}
<li><a href="{{ entry.url }}"><code>{{ entry.url }}</code></a></li>
{%- endfor %}
</ul>
#}