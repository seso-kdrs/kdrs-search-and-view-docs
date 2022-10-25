---
layout: xml
title: rows
parent: xml
---
Default number of rows is 20. To show more rows, please enter a number here to avoid getting too many pages.

{% highlight xml %}
    <table>
        <rows>1000</rows>
{% endhighlight %}

## Sorting
Beware that sorting will sort this number of rows. If you need to sort across all pages, then increase this number to avoid paging entirely. 

## Performance
Check to see if the incrased delay for the view is acceptable.

`Tip` Increase the number of rows to get them all in a pdf, or sent to printer.