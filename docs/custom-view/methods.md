---
layout: default
title: methods
parent: Ruby View
---
# Methods
These are the available methods for getting and joining data

## Get data
{% highlight erb %}
<% get_table(table, criteria,fl:,filter:nil,page:1, rows:DEFAULT_ROWS) %>
{% endhighlight %}
- fl: fields to retrieve
- criteria: Hash of criteria e.g. {school:"fro", class:"3a", year:"2001"}
- criteria can also be a set of space separated values, e.g. COURSECODE:"1 2 3" or [] for empty
- Returns empty array [] if no hits

### Example
{% highlight erb %}
<% diploma = get_table("diploma", {student_id:"123456"}, fields:"absence, school, date, location") %>
{% endhighlight %}

## Join data
Join two tables. This is similar to using the tag "lookup" in xml

{% highlight erb %}
<% join_table(main:, fk:, pk:, fl:, table:) %>
{% endhighlight %}
- main: the main table (hash) that you want to extend with more data
- fk: the foreign key in the main document
- pk: the primary key in the new table
- table: the lookup table that has additional

### Example: Let each customer have a city
{% highlight erb %}
<% customers = join_table(main:customers, fk:"address_id", pk:id", table:"address", fields:"city") %>
{% endhighlight %}

