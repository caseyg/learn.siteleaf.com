---
title: Liquid
date: 2015-10-31 20:03:00 -04:00
position: 3
layout: page
---

Liquid is an open-source templating language that was developed by [Shopify](http://shopify.com). It uses tags, objects, and filters to render out content into a theme.

For an in-depth Liquid reference, check out the [official Liquid documentation](https://docs.shopify.com/themess/liquid-documentation/basics). For a full list of tags and filters, see [Shopify's Liquid for Designers](https://github.com/Shopify/liquid/wiki/Liquid-for-Designers) wiki.

## Tags

A tag is a piece of logic that will tell the templating engine what to do. This includes operations like `if`, `for`, `foreach`, and `capture`. For example:

{% highlight liquid %}
{% raw %}
{% if page.title == 'Home' %}
  Do something if condition is true
{% else %}
  Do something if condition is false
{% endif %}
{% endraw %}
{% endhighlight %}

Note that each tag is ended with the same tag, prepended with `end`.

## Objects

An object is a piece of data that has attributes with content. An object can be your site, a post, a set of posts, and so on. For example:

{% highlight liquid %}
{% raw %}
{{ post.title }}
{% endraw %}
{% endhighlight %}

## Filters

Filters are used to modify the output of attributes (i.e., strings, numbers, variables, and objects):

{% highlight liquid %}
{% raw %}
{{ 'sales' | append: '.jpg' }}
<!-- Outputs: sales.jpg -->
{% endraw %}
{% endhighlight %}

## Further Reading

- [Shopify: Liquid wiki](https://github.com/Shopify/liquid/wiki)
- [Jekyll: Variables](http://jekyllrb.com/docs/variables/)
