---
layout: xml
title: sort
parent: Standard View
---
Sort table based on the given column. If the values seem to be integers, the sort will be numeric. If not they will sort as string.

Example:
{% highlight xml %}
    <table>
        <sort>lastname</parent> <!-- sorts in ascending order  -->
        <sort>lastname desc</parent> <!-- sorts in descending order -->
{% endhighlight %}

Currently you can sort on one column, either in ascending or descending order.
