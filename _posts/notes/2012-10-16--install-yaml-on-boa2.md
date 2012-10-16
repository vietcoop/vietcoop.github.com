---
layout: post
title: Install YAML on Barracuda
permalink: /notes/boa/install-yaml
category: 'Notes'
tags: ['system', 'barracuda', 'aegir', 'octopus', 'pecl', 'php']
published: true
---

1. Install LibYAML - http://pyyaml.org/wiki/LibYAML
2. Using pecl to install yaml

    /opt/local/bin/pecl install yaml
    echo 'extension=yaml.so' >  /etc/php5/fpm/conf.d/yaml.ini
    service php53-fpm restart
