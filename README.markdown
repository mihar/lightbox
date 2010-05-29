Lightbox Rails plugin
=====================

Introduction
------------

This plugin will add two helpers, to make it faster to use Lightbox in Rails.

Installation
------------

In order to use Lightbox, you must satisfy it's dependencies first. Lightbox needs it's Javascript file and 
the default stylesheet in order to function correctly.

Because this plugin embeds the lightbox.js into the defaults, you can simply put this line (if not there already) in the page head:

    <%= javascript_include_tag :defaults %>

You must also include the lightbox stylesheet. Add this to the page head:

    <%= stylesheet_link_tag 'lightbox' %>


Usage
-----

Use one of the two helpers provided.

    <%= lightbox_link_to "Link Name", "/path/of/your/image.png" %> 
or

    <%= lightbox_image_tag "/path/of/your/image-thumb.png", "/path/of/your/image.png", {:class=>"images"}, :title => "This is a test!", :group => "image_group" %>

The 4th argument are options for the `image_tag` and the last argument are options for the `link_to`.
