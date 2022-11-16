---
layout: xml
title: lob
parent: Default View
---
Inline lobs will be displayed automatically.\
External lobs must be specified as shown in the example.

Example:
{% highlight xml %}
    <table>
        <field>blob_field as document</field>
        <lob>
            <name>document</name>
            <index>5</index>
        </lob>
    </table>
{% endhighlight %}

Currently one blob field is supported for each table.
This will be changed in a future release.

## Get lob from another table
It is possible to `lookup` data in another table, and fetch blob data, as shown in the next example. Here we fetch both `picture` and the row number `uuid`. The `uuid` is important, so that we request the correct row.

{% highlight xml %}
   <table>
        <name>group</name>
        <fields>personid</fields>
        <lookup>
            <foreignkey>personid</foreignkey>
            <table>people</table> 
            <primarykey>id</primarykey>
            <fields>firstname,lastname,picture,uuid</fields>
        </lookup>
    </table>
    <lob>
        <name>picture</name>
        <table>people</table> <!-- blob table. Not needed if main table  -->
        <index>5</name> <!-- hover the mouse in dbptk to see the column index number  -->
    </lob>
{% endhighlight %}


Handling of blobs will improve in a future release.