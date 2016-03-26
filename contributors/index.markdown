---
layout: page
title: "Contributors"
date: 2016-03-25
comments: false
categories: [personal blog]
sharing: false

---

## Contributors

These lovely people have contributed a fix to my blog. If you want
to see yourself in this list, send me a pull request!

The people in the list below have contributed to my blog. You can contribute by posting a tech essay, [pointing out a mistake](https://github.com/yaobinwen/yaobinwen.github.io/issues/new), suggesting new ideas, or any other ways.

Every post in my blog has an edit link that lets you edit the blog post directly in the browser and automatically sends me a pull request.

Or, [visit my repository]({{site.github.repository_url}}) and send me a pull request the old fashioned way.

<ul>
{% for contributor in site.github.contributors %}
  <li>
    <img src="{{ contributor.avatar_url }}" width="32" height="32" /> <a href="{{ contributor.html_url }}">{{ contributor.login }}</a>
  </li>
{% endfor %}
</ul>
