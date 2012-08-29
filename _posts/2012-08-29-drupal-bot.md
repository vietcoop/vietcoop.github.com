---
layout: default
published: true
permalink: /documentations/tools/drupal/drupal-bot
title     : Drupal Bot
category  : 'Documentation'
tags      : ['tools', 'drupal']
---

{% include JB/setup %}

[Drupal Bot](http://drupal.org/project/bot) là một project/tool trên nền Drupal, giúp Drupal có thể vận hành bot trên các kênh IRC, sử dụng Bot khéo léo, bot trở thành công cụ rất hiệu quả, rất thú vị.

Đây là một số lệnh để điều khiểm bot:

1. Xem tình trạng bot: `drush bot-status`
1. Reset tình trạng bot: `drush bot-status-reset -y`
1. Start bot: `drush bot-start`
1. Start bot deamon: `nohup drush bot-start &`