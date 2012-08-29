---
layout: default
published: false
title: Dùng path trong custom text của views

---

Khi dùng views chúng ta đôi lúc cũng dùng customtext để add list link đến pages nào đó.

Việc dùng list link bằng cách viết tag a và link đến page khác có thể ở dưới local của bạn nó chạy được nhưng đây lên server thì nó không chạy.

Để giải quyết vấn để chúng ta có thể làm theo cách sau:

1. Thêm field mới rewrite results field này là một link và config như sau 
	* Link path : page link bạn muốn chuyển đến ư
    * Và check : Use absolute path. 
    * check Exclude from display
1. Thêm field này vào custom text dùng REPLACEMENT PATTERNS