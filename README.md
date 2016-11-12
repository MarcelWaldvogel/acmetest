# acmetest
Unit test project for le project https://github.com/Neilpang/acme.sh



# Here are the latest status:

| Platform | Status| Last Run Time| Comments|
-----------|-------|--------------|---------|
|windows-cygwin| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/windows-cygwin.svg?Sat, 12 Nov 2016 04:54:13 UTC)| Sat, 12 Nov 2016 04:54:13 UTC| Passed |
|freebsd| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/freebsd.svg?Fri, 11 Nov 2016 20:10:29 UTC)| Fri, 11 Nov 2016 20:10:29 UTC| Passed |
|openbsd| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/openbsd.svg?Sat, 12 Nov 2016 04:19:42 UTC)| Sat, 12 Nov 2016 04:19:42 UTC| Passed |
|pfsense| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/pfsense.svg?Sat, 12 Nov 2016 04:25:05 UTC)| Sat, 12 Nov 2016 04:25:05 UTC| Passed |
|solaris| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/solaris.svg?Sat, 12 Nov 2016 04:35:53 GMT)| Sat, 12 Nov 2016 04:35:53 GMT| Passed |
|ubuntu:14.04| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/ubuntu-14.04.svg?Sat, 12 Nov 2016 05:03:03 UTC)| Sat, 12 Nov 2016 05:03:03 UTC| Passed |
|ubuntu:15.04| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/ubuntu-15.04.svg?Sat, 12 Nov 2016 05:07:36 UTC)| Sat, 12 Nov 2016 05:07:36 UTC| Passed |
|ubuntu:16.04| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/ubuntu-16.04.svg?Sat, 12 Nov 2016 05:12:18 UTC)| Sat, 12 Nov 2016 05:12:18 UTC| Passed |
|ubuntu:latest| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/ubuntu-latest.svg?Sat, 12 Nov 2016 05:17:02 UTC)| Sat, 12 Nov 2016 05:17:02 UTC| Passed |
|debian:7| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/debian-7.svg?Sat, 12 Nov 2016 05:21:04 UTC)| Sat, 12 Nov 2016 05:21:04 UTC| Passed |
|debian:8| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/debian-8.svg?Sat, 12 Nov 2016 05:25:26 UTC)| Sat, 12 Nov 2016 05:25:26 UTC| Passed |
|debian:latest| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/debian-latest.svg?Sat, 12 Nov 2016 05:29:40 UTC)| Sat, 12 Nov 2016 05:29:40 UTC| Passed |
|centos:5| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/centos-5.svg?Sat, 12 Nov 2016 05:32:47 UTC)| Sat, 12 Nov 2016 05:32:47 UTC| Passed |
|centos:6| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/centos-6.svg?Sat, 12 Nov 2016 05:37:11 UTC)| Sat, 12 Nov 2016 05:37:11 UTC| Passed |
(The openssl in CentOS 5 doesn't support ECDSA, so the ECDSA test cases failed. However, RSA certificates are working there.)

# How to run tests

First point at least 2 of your domains to your machine, 
for example: `aa.com` and `www.aa.com`

And make sure 80 port is not used by anyone else.

```
cd acmetest
TestingDomain=aa.com   TestingAltDomains=www.aa.com  ./letest.sh
```

# How to run tests in all the platforms through docker.

You must have docker installed, and also point 2 of your domains to your machine.

Then test all the platforms :

```
cd acmetest
TestingDomain=aa.com   TestingAltDomains=www.aa.com  ./rundocker.sh  testall
```

The script will download all the supported platforms from the official docker hub, then run the test cases in all the supported platforms.

Then test single docker platform :

```
cd acmetest
TestingDomain=aa.com   TestingAltDomains=www.aa.com  ./rundocker.sh  testplat   centos:latest
```









