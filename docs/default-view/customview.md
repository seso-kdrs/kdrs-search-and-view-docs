---
layout: xml
title: customview
parent: Default View
---
You can make a custom view if you want advanced layout or features.
Make a file e.g. `views/_schoolsys_diploma.html.erb`
You can edit both the data and the presentation.

{% highlight xml %}
    <table>
        <customview>diploma</customview>
{% endhighlight %}

Data from the xml file will be available in `@docs`