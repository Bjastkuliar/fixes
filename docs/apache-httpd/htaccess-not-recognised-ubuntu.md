---
author: ''
category: Apache-Httpd
date: '2015-01-18'
summary: ''
title: Htaccess Not Recognised Ubuntu
---

Apache is not recognising .htaccess 
===================================

1. In the directory tag for the configuration (vhost) must contain ` Override All `

2. in apache.conf, this line is uncommented
 ` AccessFileName .htaccess `

3. Search for AllowOverride in apache.conf
Change ` AllowOverride None ` to ` AllowOverride all ` in relevant cases
