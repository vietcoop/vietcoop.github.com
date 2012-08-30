---
layout: post
published: true
permalink: /notes/drupal-7/reset-password
title: Reset password ở Drupal 7
category: 'Notes'
tags: ['faq', 'drupal 7', 'drush']
author: andytruong
comments: true
published: true
---

{% include JB/setup %}

Rất có thể bạn mất mật khẩu ở Drupal 7 app của mình. Có nhiều cách để lấy lại nó:

1. Sử dụng tính năng reset password bằng trang /user/password. Tuy nhiên, nếu mailer của hệ thống bạn gặp trở ngại, bạn sẽ không thể sử dụng cách này. 
2. Sử dụng [Drush](http://drush.ws/) - mở ứng dụng bash/terminal, di chuyển thư mục hiện hành đến nơi chứa settings.php của Drupal, thí dụ nó là /var/www/sites/default/, bạn sẽ cần thực hiện các lệnh sau:

    cd /var/www/sites/default
    drush user-login drupaladmin

Drush sẽ cung cấp cho bạn đường dẫn để reset lại password. Thay đổi drupaladmin thành username tương ứng cần phục hồi.

Andy Truong