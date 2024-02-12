---
layout: default
title: variables
parent: Ruby View
---
# Variables
These are the available variables
{: .fs-6 .fw-300 }

## @docs
Hash containing the data from XML
### Example - display the @docs variable
{% highlight erb %}
<%= render 'table', vi: @vi, ti: @ti %>
{% endhighlight %}


## @show_fields
Array of fields to present in the table

### Example - adding and removing fields
{% highlight erb %}
<%      
    @showfields += ["first name", "last name"] # will add to the exising
    @showfields -= ["first name", "last name"] # will remove these columns
    @showfields = ["first name", "last name"] # will redefine all visible columns
    @showfields << "my column"  # a simple way to add just one column
%>
{% endhighlight %}
