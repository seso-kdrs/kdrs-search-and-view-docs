---
layout: xml
title: customview
parent: XML Template
---
You can make a custom view if you want advanced layout or features.
Make a file e.g. `vendor/school_app/_diploma.html.erb`
You can edit both the data and the presentation.
See section "Ruby Template" in documentation.

{% highlight xml %}
    <table>
        <customview>diploma</customview>
{% endhighlight %}

Data from the xml file will be available in `@docs`