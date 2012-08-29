---
layout: post
published: true
title : Sử dụng openshift
permalink: /documentation/tools/openshift
author    : duynguyen
comments  : true
---

# Openshift là gì

nó là môi trường để bạn tạo và phát triển ứng dụng của bạn trên clound.

## Giá cả thế nào?
 Openshift cung cấp 2 loại tài khỏan FreeShift và MegaShift
 
1. FreeShift miễn phí 3 Gears : nó đử dung lương để cho ta có thể chạy một site drupal thông thường
2. MegaShift : bạn có thể tham khảo tại đây https://openshift.redhat.com/community/developers/pricing

## làm sao để dùng Openshift
Bạn chỉ cần đăng ký 1 tài khỏan và có thể sủ dụng openshift.

## Open shift hỗ trợ những gì
openshift cho chúng ta tạo các Instant Applications sau:

1. CakePHP
1. Ruby on Rails
1. Ruby on Rails
1. Kitchensink Example
1. WordPress
1. Drupal

Và các Web Cartridges

1. Ruby 1.9.3
1. PHP-5.3
1. Python 2.6
1. Perl 5.10
1. .....

## Làm sao để tạo một ứng dụng. ở đây tôi chỉ đề cập đến drupal
Có 2 cách để tạo một ứng dụng trên openshift
1. Dùng giao diện web để quản lý
1. Dùng dòng lệnh . bạn có thể tham khảo link sau để cài đặt client tool https://openshift.redhat.com/community/get-started . sau khi cài đặt bạn có thể gõ chưa gõ rhc --help để xem danh sách lệnh của nó.

## Làm để quản lý database, source của ứng dụng
Openshift không hỗ trợ chúng ta fpt vào ứng dụng của chúng ta vì thế bạn chỉ có thể tác động đến source và database như sau:

1. Bạn có thể add cartridge php myadmin để quản lý database
1. Dùng shh để connecnt vào app của bạn
1. Dùng git để quản lý source



	                                                                  by duynguyen