Title: IE sendkeys 慢的解决办法
Date: 2010-12-03 10:20
Modified: 2010-12-05 19:30
Category: Selenium
Tags: selenium
Slug: selenium1
Authors: Quan
Summary: Short version for index and feeds


在IE 11上使用selenium发现sendKeys的时候超级的慢，
根本原因是IE 64 位的驱动有BUG， 会使得在IE11上这个操作很慢。
换成了 32 位的驱动解决。
下载地址：
[InternetExplorerDriver](http://selenium-release.storage.googleapis.com/index.html)

Please make sure that this is available on your $PATH
(or %PATH% on Windows) in order for the IE Driver to work as expected.
