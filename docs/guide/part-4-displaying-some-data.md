---
layout: guide
title: "Part 4: Displaying some data"
nav_order: 5
parent: Guide
---
Now we will actually show some information stored in the database.\
The following image shows a schema of all the tables in our database:\
<br>
![](../../../assets/images/guide/dbptk-schema.png)

*The database schema is from DBPTK, and is found by clicking "BROWSE" in the database overview*\
<br>
The table *film* looks interesting, so we will click that to view it:\
<br>
![](../../../assets/images/guide/dbptk-film-table.png)
<br>
Our first task will be to show the title and description of every film in a table.
<br>
1. To do this, we have to start by defining a new table for our view. We do this by adding a `<tables>` tag containing one `<table>` tag in our XML template:

{% highlight xml %}
<root>
    <views>
        <view>
            <name>Den beste visningen</name>
            <tables>
                <table>                    
                </table>
            </tables>
        </view>
    </views>
</root>
{% endhighlight %}

{: style="counter-reset: step-counter 1;" }
2. Within the `<table>` tag, there are 4 required tags we need to specify. These are `<name>`, `<heading>`, `<primarykey>` and `<fields>`.\
The purpose of these tags is as follows:
<br>
  
| XML tag | Value |
| ----- | ---------- |
| `<name>` | The name of the table in the database we want data from. As we are getting data from the table *film*, the value will be `film`|
| `<heading>` | The name that will be displayed above our table. This can be set to anything you want. |
| `<primarykey>` | A primary key is a column that has a unique value for every row in a table. For the *film* table the unique column is *film_id*, so we have to set the primary key to `film_id` |
| `<fields>` | This is a list of columns we want to show data from. The list is comma-separated, so because we want to show data from the columns *title* and *description*, we have to set fields to `title, description` | 



{: style="counter-reset: step-counter 2;" }
3. Update the XML template file with the required tags: 
{% highlight xml %}
...
<table>
    <name>film</name>
    <heading>Den beste tabellen</heading>
    <primarykey>film_id</primarykey>                    
    <fields>title, description</fields>
</table>
...
{% endhighlight %}
*Some parts of the XML file that were not changed in this step have been omitted.*