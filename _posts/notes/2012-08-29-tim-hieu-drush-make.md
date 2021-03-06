---
layout: default
published: true
title : Tìm hiểu về Drush Make
permalink: /notes/tools/drush-make
comments  : true
author    : pvmchau
category  : 'Notes'
tags      : ['tools', 'drush', 'drush make']
---

# Drush Make

The __Dru__pal __Sh__ell is a command line tool. Drush Make is a macro for installing Drupal.

- Công dụng của Drush Make: bạn có thể cài đặt
	- Drupal Core, distributions or profiles.
	- Modules, themes or features.
	- Patches.
	- External libraries.
	- git/ bzr/ SVN/ CVS repositories
	- Other drush makefiles.

- Sử dụng Drush Make. Có 2 cách để chạy Drush Make trên site của bạn:
	- Download Drush Make
	- Sử dụng Drush Command
	- Bên cạnh đó bạn có thể thông qua trang web http://drushmake.me/ để tạo ra 1 file make.

- Cấu trúc của lệnh Drush Make: $ drush make -h
- Tạo mới 1 file Drush Make cho site hiện tại: $ drush generate-makefile myfile.make
>	; Make file for Art Websites.
>	api = 2
>	core = 6.x

>	projects[drupal][version] = "6.19"

>	; Modules
>	; Because you will always be using these two contributed modules.
>	projects[views][subdir] = "contrib"
>	projects[views][version] = "2.11"

>	projects[cck][subdir] = "contrib"
>	projects[cck][version] = "2.8"
Vd: 1 file make đơn giản

- Setup 1 site drupal mới từ 1 file Drush Make: $ drush make  myfile.make
- Thêm 1 module vào trong file make

>	projects[flag][subdir] = contrib
>	projects[flag][version] = 2.0-beta5
>	; DEVELOPMENT
>	projects[devel][subdir] = "dev" 

- Cập nhật 1 bản patch
>	; http://drupal.org/node/968826#comment-3863422
>	projects[features][patch][] = "http://drupal.org/files/issues/968826 ... 

- Tải file vào thư viện của site

>	; jQuery UI
>	libraries[jquery_ui][download][type] = "get"
>	libraries[jquery_ui][destination] = "modules/contrib/jquery_ui"
>	libraries[jquery_ui][download][url] = "http://jquery-ui.googlecode.com/files/jquery-ui->	1.7.3.zip"
>	libraries[jquery_ui][directory_name] = "jquery.ui" 

- Các version control khác

>	projects[ccpc2011][type] = "theme"
>	projects[ccpc2011][download][type] = "git"
>	projects[ccpc2011][download][url] = "http://mydomain/mytheme.git"
>	projects[ccpc2011][download][branch] = "dev" 

## Quick tips
- Drush --help:
>	drush command --help

- DB Dump:
>	$ drush sql-dump > database-backup-$(date +%Y-%m-%d-%H.%M.%S).sql

- Import a Database:
>	drush sqlc < database_file.sql

- Drush password reset URL:
>	drush php-eval 'echo user_pass_reset_url(user_load(1));'

- Take site offline:
>	drush vset --always-set site_offline 1

## Resource:
- Get the code drush_make
- Drush FAQ's and Documentation drush.ws 
- Generate a make file drushmake.me 

## Chạy Drush Make trên server Unix
- Drush Make chỉ được hỗ trợ trên drush 5.x trở lên
1. Kiểm tra version hiện tại của drush: 
>	$ drush --version
1. Download phiên bản mới nhất của drush tại http://drupal.org/project/drush
>	$ wget http://ftp.drupal.org/files/projects/drush-7.x-5.7.tar.gz 
1. Giải nén thư mục drush-xxx.taz.gz vừa download về:
>	$ tar zxf drush-xxx.tar.gz
1. Kiểm tra version của file vừa download
>	$ ./drush/drush --version
1. Tạo alias mới cho drush mới
>	$ vim ~/.bashrc
>	$ alias drush="/home/yourdir/drush/drush"

@__pvmchau__