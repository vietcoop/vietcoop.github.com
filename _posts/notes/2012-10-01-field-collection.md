---
layout: post
published: true
title : Field Collection module for Drupal 7
comments: true
category: 'Notes'
tags: ['drupal', 'drupal 7', 'module', 'snippets', 'development']
permalink: /notes/drupal/7/field-collection
author: andytruong
---

{% include JB/setup %}

[Field Collection](http://drupal.org/project/field_collection "") is an excellent module of Drupal, which:

> Provides a field-collection field, to which any number of fields can be attached.
> 
> A field collection is internally represented as an entity, which is embedded in 
> the host entity. Thus, if desired field collections may be viewed and edited 
> separately too.

Sometime you want to create **field collection entities** dynamicly, this is trick to create/update/delete field collection entities

  <script src="https://gist.github.com/3792605.js?file=gistfile1.php">
  </script>
