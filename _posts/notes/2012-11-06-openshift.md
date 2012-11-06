---
layout: post
published: true
title : Sử dụng OpenShift - Notes
permalink: /notes/services/openshift
author    : duynguyen
category: Notes
tags: ['paas', 'cloud']
comments  : true
---

### Openshift là gì

Openshift là môi trường để bạn tạo và phát triển ứng dụng của bạn trên cloud.

### Giá cả thế nào?

Openshift cung cấp 2 loại tài khỏan FreeShift và MegaShift

1. FreeShift miễn phí 3 Gears : nó đử dung lương để cho ta có thể chạy một site drupal thông thường
2. MegaShift: bạn có thể tham khảo [tại đây](https://openshift.redhat.com/community/developers/pricing).

### Làm sao để dùng Openshift

Bạn chỉ cần đăng ký 1 tài khoản và có thể sủ dụng openshift. Mỗi account 

### Open shift hỗ trợ những gì

OpenShift cho chúng ta tạo các Instant Applications sau:

1. Drupal
1. CakePHP
1. Ruby on Rails
1. Kitchensink Example
1. WordPress

Và các Web Cartridges

1. Ruby 1.9.3
1. PHP-5.3
1. Python 2.6
1. Perl 5.10
1. …

### Làm sao để tạo một ứng dụng, ở đây tôi chỉ đề cập đến Drupal?

Có 2 cách để tạo một ứng dụng trên Openshift:

1. Dùng giao diện web để quản lý
1. Dùng dòng lệnh . bạn có thể tham khảo link sau để cài đặt [client tool](https://openshift.redhat.com/community/get-started). Sau khi cài đặt bạn có thể gõ chưa gõ rhc --help để xem danh sách lệnh của nó.

### Làm để quản lý database, source của ứng dụng

Openshift không hỗ trợ chúng ta fpt vào ứng dụng của chúng ta vì thế bạn chỉ có thể tác động đến source và database như sau:

1. Bạn có thể add cartridge php myadmin để quản lý database
1. Dùng shh để connect vào app của bạn
1. Dùng git để quản lý source

### Examples

1. [Redis](https://github.com/openshift/redis-openshift-example)
1. [Drupal](https://github.com/openshift/drupal-example)
1. [DokuWiki](https://github.com/openshift/dokuwiki-quickstart)
1. [Redmine](https://github.com/openshift/redmine-2.0-openshift-quickstart)

by **DuyNguyen**