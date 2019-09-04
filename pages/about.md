---
layout: page
title: About
description: A computer science student's personal blog, including what I've thought, learned from work and study. You can contact me with my working email, caucherw@gmail.com.
keywords: Zeyu Wang, 王泽宇
comments: false
menu: 关于
permalink: /about/
---



## 联系

{% for website in site.data.social %}
* {{ website.sitename }}：[@{{ website.name }}]({{ website.url }})
{% endfor %}

## Skill Keywords

{% for category in site.data.skills %}
### {{ category.name }}
<div class="btn-inline">
{% for keyword in category.keywords %}
<button class="btn btn-outline" type="button">{{ keyword }}</button>
{% endfor %}
</div>
{% endfor %}
