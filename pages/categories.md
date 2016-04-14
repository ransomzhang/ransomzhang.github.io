---
layout: categories
title: Categories
description: 哈哈，你找到了我的文章基因库
keywords: 分类
comments: false
menu: 分类
permalink: /categories/
---
> 我希望中国的读书人，无论你读什么，能早日养成自己的兴趣，一生内心有些倚靠，日久产生沉稳的判断力。这么大的国家，这么多的人，这么复杂，环环相扣的历史，再也不要用激情决定国家及个人的命运；我还盼望年轻人能培养一个宽容、悲悯的胸怀。让孩子从幼年开始，喜欢上读书，也是如此。——齐邦媛

<section class="container posts-content">
{% assign sorted_categories = site.categories | sort %}
{% for category in sorted_categories %}
<h3>{{ category | first }}</h3>
<ol class="posts-list" id="{{ category[0] }}">
{% for post in category.last %}
<li class="posts-list-item">
<span class="posts-list-meta">{{ post.date | date:"%Y-%m-%d" }}</span>
<a class="posts-list-name" href="{{ post.url }}">{{ post.title }}</a>
</li>
{% endfor %}
</ol>
{% endfor %}
</section>
<!-- /section.content -->
