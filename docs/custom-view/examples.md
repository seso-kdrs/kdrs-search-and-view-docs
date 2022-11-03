---
layout: default
title: examples
parent: Custom View
---

# Examples
These are som frequently used code snippets for the custom view.
{: .fs-6 .fw-300 }

# Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}


# Display the main table
The `@docs` variable from xml will be written to screen in standard table format.
{% highlight erb %}
<%= render 'table', vi: @vi, ti: @ti %>
{% endhighlight %}

`@vi` (view index) and `@ti` (table index) provides the user context, and is automatically fetched from the url.


