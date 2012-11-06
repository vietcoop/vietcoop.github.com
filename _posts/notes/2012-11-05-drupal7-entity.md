---
layout: post
author: andytruong
permalink: /notes/drupal-entity
title     : Entity - Drupal 7
category  : 'Documentation'
tags      : ['api', 'sub system', 'drupal 7']
published: true
---

## Core

1. [hook_entity_info](http://goo.gl/ZzZll). Examples:

    1. [search_api_entity_info](http://goo.gl/CAGSs)
    1. [profile2_entity_info](http://goo.gl/bokMS)

1. [hook_entity_info_alter](http://goo.gl/lHdxV)

### Base Classes/Interfaces

1. [DrupalEntityControllerInterface](http://goo.gl/cLsak)
1. [DrupalDefaultEntityController](http://goo.gl/y0gjP)

### Helper functions

1. [entity_create_stub_entity](http://goo.gl/fgh3X)
1. [entity_extract_ids](http://goo.gl/Mt5i1)
1. [entity_get_controller](http://goo.gl/e7BHy)
1. [entity_get_info](http://goo.gl/Qsc4Y)
1. [entity_label](http://goo.gl/aQrbH)
1. [entity_language](http://goo.gl/DQCZn)
1. [entity_load](http://goo.gl/zQgGo)
1. [entity_load_unchanged](http://goo.gl/vg1zY)
1. [entity_prepare_view](http://goo.gl/jY875)
1. [entity_info_cache_clear](http://goo.gl/aOXCe)
1. [entity_uri](http://goo.gl/tL6Ao)

## [Entity API module](http://goo.gl/l3jtF)

### Extra supported keys in hook_entity_info()

1. [entity_crud_hook_entity_info](http://goo.gl/mfH94)
1. [entity_metadata_hook_entity_info](http://goo.gl/5SOT0)
1. [hook_entity_property_info](http://goo.gl/1AcqI)
1. [hook_entity_property_info_alter](http://goo.gl/qlkmd)
1. [hook_entity_views_field_handlers_alter](http://goo.gl/K6fmg)

### Base Classes

1. [Entity](http://goo.gl/EGDUt)
1. [EntityAPIController](http://goo.gl/rGk4u)
1. [EntityAPIControllerExportable](http://goo.gl/Lg8HC)
1. [EntityDefaultUIController](http://goo.gl/04Fzh)

### Helper functions

1. [entity_metadata_wrapper](http://goo.gl/SDy40)
1. [entity_property_query](http://goo.gl/RCFHv)

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

## Tutorials

1. [Creating your own entities with Entity API](http://goo.gl/maquD)

## Extra modules

1. [ECK](http://goo.gl/68df1)
1. [Entity Cache](http://drupal.org/project/entitycache)
1. [EntityFieldQuery Views Backend](http://drupal.org/project/efq_views)
1. [Field Collection](http://drupal.org/project/field_collection)
1. [Field Collection Table](http://drupal.org/project/field_collection_table)
1. [Field Collection View](http://drupal.org/project/field_collection_views)
1. [Field Group](http://drupal.org/project/field_group)
1. [Features](http://drupal.org/project/features)
1. [Model](http://drupal.org/project/model)
1. [Search API](http://drupal.org/project/search_api)

### Modules built on EntityAPI

1. [Fieldable Panels Panes](http://drupal.org/project/fieldable_panels_panes)
1. [Subs](http://drupal.org/project/subs)
