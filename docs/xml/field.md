---
layout: xml
title: field
parent: xml
---
Specifies one field to be edited

{% highlight xml %}
    <table>
        <name>cities</name>
        <fields>name,date</fields>
        <edit>
            <field>name.capitalize</field>
            <field>date[0..9]</field>
        </edit>
    </table>
{% endhighlight %}
