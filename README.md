Jekyll Category Pages Generator
===================
This plugin generates pages for each of the categories of your site, as defined in their YAML front matter.
If enabled through configuration, it will also generate the appropriate pagination

To enable category pages generation, add the following in your _config.yml

    category_path: "categories/:cat"

If you want to customise the numbered page name, you can use the following:
Default is "page:num"

    category_page_path: "page:num"

Customise those to suit your needs, but you need to keep the placeholders as they are:  ":cat" ad ":num"

To enable pagination and define the number of posts per page, use:

    paginate_categories: 4

This plugin uses the standard Jekyll paginator, so you can also print pagination links by simply add the following in your category_index.html template:

    {% if paginator.total_pages > 1 %}
    <nav class="pagination">
      {% if paginator.previous_page_path %}
        <a class="button previous" href="{{ paginator.previous_page_path }}" title="Previous posts">previous </a>
      {% endif %}

      {% if paginator.next_page_path %}
        <a class="button next" href="{{ paginator.next_page_path }}" title="Next posts"> next</a>
      {% endif %}
    </nav>
    {% endif %}


Initially based on https://github.com/mwotton/lambdamechanic-jekyll and modified to suit a different site and categories architecture


Author
======

Mathieu Davy :: hello@ekynoxe.com :: [@ekynoxe](http://twitter.com/ekynoxe)


Copyright
=========

Copyright (c) 2014 Mathieu Davy. See [Licence](https://github.com/ekynoxe/JekyllCategoriesTag/blob/master/LICENCE) for details.