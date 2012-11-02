---
layout: post
author: andytruong
permalink: /notes/drupal-entity
title     : Entity - Drupal 7
category  : 'Documentation'
tags      : ['api', 'sub system']
published: true
---

1. [hook_entity_info](http://goo.gl/ZzZll)

### [Entity API module](http://goo.gl/l3jtF)

### Extra supported keys in hook_entity_info()

1. [entity_crud_hook_entity_info](http://goo.gl/mfH94)
1. [entity_metadata_hook_entity_info](http://goo.gl/5SOT0)

### Base Classes

1. [DrupalDefaultEntityController](http://goo.gl/y0gjP)
1. [Entity](http://goo.gl/EGDUt)
1. [EntityAPIController](http://goo.gl/rGk4u)
1. [EntityAPIControllerExportable](http://goo.gl/Lg8HC)

### Default Callbacks

1. entity_metadata_form_entity_ui()
1. entity_metadata_entity_get_properties()
1. entity_metadata_create_object()
1. entity_metadata_field_get_language()
1. entity_metadata_field_options_list()
1. entity_metadata_field_property_get()
1. entity_metadata_field_property_set()
1. entity_metadata_field_query()
1. entity_metadata_field_verbatim_get()
1. entity_metadata_field_verbatim_set()
1. entity_metadata_status_options_list()
1. entity_metadata_view_single()
1. entity_metadata_table_query()

### Tutorials

1. [Creating your own entities with Entity API](http://goo.gl/maquD)

### Extra modules

1. [ECK](http://goo.gl/68df1)
