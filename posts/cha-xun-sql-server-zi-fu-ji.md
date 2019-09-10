---
title: '查询SQL Server字符集'
date: 2019-09-05 09:32:52
tags: []
published: true
hideInList: false
feature: https://uploadbeta.com/api/pictures/random
---
* 1
SELECT COLLATIONPROPERTY('Chinese_PRC_Stroke_CI_AI_KS_WS', 'CodePage')
下面是查询结果：
936 简体中文GBK
950 繁体中文BIG5
437 美国/加拿大英语
932 日文
949 韩文
866 俄文
65001 unicode UFT-8
* 2
use master
select SERVERPROPERTY(N'edition') as Edition --数据版本，如企业版、开发版等
,SERVERPROPERTY(N'collation') as Collation --数据库字符集
,@@VERSION as Version --数据库版本号
,@@LANGUAGE AS Language --数据库使用的语言，如us_english等
,SERVERPROPERTY(N'servername') as ServerName --服务名
* 333
SELECT a.NAME AS 表名,b.NAME AS 列名,a.COLLATION FROM syscolumns a,sysobjects b
WHERE a.id=b.id  and b.NAME='tcr0021'  ORDER BY 3 desc