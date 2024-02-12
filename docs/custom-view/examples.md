---
layout: default
title: examples
parent: Ruby View
---

# Examples
These are som frequently used code snippets for the custom view.
{: .fs-6 .fw-300 }

# Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}


## Display the main table
{% highlight erb %}
<%= render 'table', vi: @vi, ti: @ti %>
{% endhighlight %}
- Will write the content of variable `@docs` that come from xml

## Add a new column for full name
Make a new column that combines first name and last name
{% highlight erb %}
<%
    docs.each do |doc|
      doc["full name"] = doc["first name"] + " " + doc["last name"]
    end
    @show_fields << "full name"
%>
{% endhighlight %}

## Provide an alternative value
Show the student grade if it exists, or show a dashed line if its missing
{% highlight erb %}
<%
    docs.each do |doc|
      doc["grade"] ||= "-----"
    end
    @show_fields << "full name"
%>
{% endhighlight %}

## Use the first part of the string
E.g. remove time from the string 12.02.2024 11:00
{% highlight erb %}
<%
    docs.each do |doc|
      doc["date"] = doc["date"][0..9]
    end
%>
{% endhighlight %}

## Convert utc date to local time zone
We make a custom method, and use this in the documents loop.
{% highlight erb %}
def utc_to_local_time(date)
    Date.parse(date).in_time_zone('Europe/Oslo')
end
<%
    docs.each do |doc|
      doc["date"] = utc_to_local_time(doc["date"])
    end
%>
{% endhighlight %}


