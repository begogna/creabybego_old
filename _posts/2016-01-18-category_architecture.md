---
layout: default
title: Architecture
date:   2016-01-18 01:00:00
excerpt: "Architecture"
#last modified: 2013-05-31
categories: ['indice_categorias']
tags: indice_categorias
image:
  feature: room.jpg
  topPosition: 0px
bgContrast: dark
bgGradientOpacity: darker
syntaxHighlighter: no
---


<section class="section--first section--frontpage">
  <div class="section-title">
    <div class="container">
      <h1>
        {{ site.name }}
      </h1>
      <div class="postMeta-wrapper postMeta-wrapper--frontpage">
        <ul class="postMeta">
          <li class="postMeta-tagline">
            3D artist and visual designer
          </li>
        </ul>
      </div>
    </div>
  </div>
</section>
<section class="section--postsWrapper">
  <div class="container">
    <div class="blockGroup">
      <ul class="blockGroup-list">
        {% for post in site.categories.architecture %}
          <li class="block-medium">
            <div class="postArticle-wrapper">
              <article class="postArticle postArticle--short">
                {% if post.image.feature %}
                  <a href="{{ post.url }}">
                    <div class="postArticle-image desaturate" style="background-image:url('{{ post.image.feature | prepend: site.baseurl_featured_img }}')">
                    </div>
                  </a>
                {% else %}
                <a href="{{ post.url }}">
                  <div class="postArticle-image" style="background-image:url('{{site.baseurl}}assets/images/logo-black.svg')">
                  </div>
                </a>
                {% endif %}
                <a class="postArticle-title" href="{{ post.url }}">{{ post.title }}</a>
              </article>
              <div class="block-postMeta">{{ post.date | date_to_string }}</div>
            </div>
          </li>
        {% endfor %}
      </ul>
    </div>
  </div>
</section>
