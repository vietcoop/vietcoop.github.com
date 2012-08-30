---
layout: post
published: true
permalink:/documentation/faq/drupal-7/memcached-and-form
title: Các công cụ đang được sử dụng tại Viet Coop
comments: true
author: andytruong
category: 'Documentation'
tags: ['tools', 'development', 'memcached']
published: true
---

{% include JB/setup %}

Hôm nay tôi gặp một lỗi khá đơn giản, nhưng lại tốn rất nhiều thời gian để khắc phục: Mọi form sử dụng __/system/ajax__ đều không hoạt động. Khi gặp trường hợp gì đó bất thường, tôi thường kiểm tra lại cấu hình nginx, xem có bị cache gì đó ở phía nginx hay không. Nhưng kiểm tra tới, kiểm tra lui, không thấy có nginx nó cache gì hết.

Tức mình, tôi thử sử dụng cùng mã nguồn đang sử dụng, cài lại Drupal. Và thử tính năng "Add more choice" của poll.module. Thật lạ, nó cũng không hoạt động.

Quá bối rối. Tôi nghĩ nâng cáp Barracuda lên Head sẽ giải quyết được vấn đề. Tôi liền thử. Kết quả của việc thử nghiệm này, tôi tốn thêm một đống thời gian nữa. Memcache không compile và nhiều thư viện khác nữa, thiếu tùm lum hết!

Bối rối càng thêm bối rối, tôi cố gắng cài lại bản Barracuda cũ.... hì hục hì hục, ... Thôi thì làm cái chiêu cần làm nhất mà lúc đầu tôi lười biếng: debug từng bước. Thật may mắn, tôi phát hiện ra, sau hàm lấy form từ cache, kết quả form trả về là rỗng. Từ đây, tôi xem lại phần cấu hình, anh chàng memcache đang được sử dụng. Đến đây, tôi đã xác định được hung thủ. Thử chuyển cache về lại database bình thường, lỗi không còn.

Tôi và issues list của memcache.module tìm kiếm, thì tìm được [ticket này](http://drupal.org/node/1214536#comment-4748042). Túm lại cách fix: Thêm vào file settings.php dòng này:

    $conf\['cache_class_cache_form'\] = 'DrupalDatabaseCache';

Dòng lệnh nhằm xác định, Drupal cần lấy class DrupalDatabaseCache để handle việc truy cập cache.

Lý do cụ thể hơn, các bạn có thể [tìm hiểu thêm ở đây](http://drupal.org/node/512026).

Andy Truong

__Update:__ Thì ra issue này đã được đưa vào [README.txt](http://drupalcode.org/project/memcache.git/blob/5947cf0d625628b2423237baabe512984114a7a7:/README.txt)