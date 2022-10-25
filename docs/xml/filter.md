---
layout: xml
title: filter
parent: xml
---
Data can be filtered. This will be sent as query to the database. \
solr syntax can be used, but use human display names for the fields. \

Example: Show the subjects for a student that are related to his/her final year. Also include exams.
{% highlight xml %}
    <table>
        <name>activity</name>
        <filter>type:s || type:e</filter>        
{% endhighlight %}

Example: Include all buildings that have the name `school`
{% highlight xml %}
    <table>
        <name>buildings</name>
        <filter>name:"school"</filter>        
{% endhighlight %}



Currently multiple lines of filtering is not supported. Please use `&&`, `||` to combine values.