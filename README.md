# Choerodon java base docker image

just used to arm64v8

change:
1、change the base image to adoptopenjdk/openjdk8-openj9:aarch64-debianslim-jre8u-nightly
2、when I build ,the aliyun mirrors always error:
Err:5 http://mirrors.aliyun.com/debian-security buster/updates/main arm64 Packages
  File has unexpected size (32 != 239192). Mirror sync in progress? [IP: 113.16.214.239 80]
  Hashes of expected file:
   - Filesize:239192 [weak]
   - SHA256:71588b492e1e5fa8d697538a565bdd65bfc221128cf69ef46d7784988578e870
   - MD5Sum:0cafd8320f3b68cf8db128948c423edd [weak]
  Release file created at: Mon, 09 Nov 2020 22:01:25 +0000
Fetched 7,982 kB in 4s (2,157 kB/s)
Reading package lists...
E: Failed to fetch http://mirrors.aliyun.com/debian-security/dists/buster/updates/main/binary-arm64/Packages.xz  File has unexpected size (32 != 239192). Mirror sync in progress? [IP: 113.16.214.239 80]
   Hashes of expected file:
    - Filesize:239192 [weak]
    - SHA256:71588b492e1e5fa8d697538a565bdd65bfc221128cf69ef46d7784988578e870
    - MD5Sum:0cafd8320f3b68cf8db128948c423edd [weak]
   Release file created at: Mon, 09 Nov 2020 22:01:25 +0000
E: Some index files failed to download. They have been ignored, or old ones used instead.


so, I chagne the mirrors to mirrors.163.com
