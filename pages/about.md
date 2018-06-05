---
layout: page
title: About
description: 学以致用，知行合一
keywords: 代强, Qiang Dai, 个人博客，IT
comments: false
menu: 关于
permalink: /about/
---

我是代强，
生而学，学而用，用然优，
坚信学以致用，知行合一的道理，
丰富知识，思考见解，
快乐生活每一天！
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
