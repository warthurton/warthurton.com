---
layout: post
title:  "Restart SQL Server DB Mail"
date:   2019-08-27 14:02:06 -0500
categories: sqlserver
published: yes
---
SQL Server DB Mail will occasionaly use a crazy amount of memory and/or resources.  I have added the following to SQL Servers for years as an Agent Job.

{% highlight sql %}
--Stop DBMail
use msdb;
go
execute dbo.sysmail_stop_sp;
go

--Start DBMail
use msdb;
go
execute dbo.sysmail_start_sp;
go

--Check the status of DBMail
use msdb;
go
execute sysmail_help_status_sp;
go
{% endhighlight %}
