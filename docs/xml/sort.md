---
layout: xml
title: sort
parent: xml
---
Sort table based on the given column. If the values seem to be integers, the sort will be numeric. If not they will sort as string.

Example:
{% highlight xml %}
    <table>
        <sort>lastname</parent> <!-- sorts in ascending order  -->
        <sort>lastname desc</parent> <!-- sorts in descending order -->
{% endhighlight %}

Currently you can sort on 1 column, thus pick 1 of the lines above.
