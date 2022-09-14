## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:7b309e8d4b9211167fbe16d983abbd40df49181c7b93e02c22e5e712291219e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull eclipse-temurin@sha256:b493f5d261c0b38686614064d54d19b3db3624c64539c44fa9b8869784e80735
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142809926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722266e726f6dbf48430e9e8da933ffa27a0e466be5c74a099e13aab8e0b1383`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 16:03:00 GMT
SHELL [cmd /s /c]
# Wed, 14 Sep 2022 16:03:01 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Wed, 14 Sep 2022 16:03:02 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 Sep 2022 16:03:03 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 16:03:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Sep 2022 16:03:17 GMT
USER ContainerUser
# Wed, 14 Sep 2022 16:07:36 GMT
COPY dir:8b6137b055df5a3c6f914a172c41a8287046696fe7ccc91d96608246e3752adc in C:\openjdk-8 
# Wed, 14 Sep 2022 16:07:47 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:233f09b2a52487084f2cfb5e06dac2815651432c9d37c729582f59cfcf66b243`  
		Last Modified: Wed, 14 Sep 2022 16:47:12 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5f2639c64b1776b5dfe2fed5337a170813f0cdd34d2c64e1d09d9f5235cfd7`  
		Last Modified: Wed, 14 Sep 2022 16:47:12 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bddf94e1bc64c713ddb831c498bf2985d3940b90388fe62a5448634a3029de5`  
		Last Modified: Wed, 14 Sep 2022 16:47:12 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a1f1420279874a6769cb079551b9385360ae7d99f1a9b0dc78951598c6f3e1`  
		Last Modified: Wed, 14 Sep 2022 16:47:09 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfdff05f1a5726e5ff4036ba1424cfb9ad2042d66409944208940778e9f2f44`  
		Last Modified: Wed, 14 Sep 2022 16:47:09 GMT  
		Size: 67.7 KB (67699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f1f515c09bdf163cdbd4255998677066f41203ed33721d156b2f3b6bfe3374`  
		Last Modified: Wed, 14 Sep 2022 16:47:09 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98644c55263d445ed9c4401727fa3089428ae59d43e08d57f05369b9c1f47033`  
		Last Modified: Wed, 14 Sep 2022 16:48:15 GMT  
		Size: 39.3 MB (39321832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3854a5524614a6286f6de420d946964efbac5682a4885b6d4669443dc3f77cab`  
		Last Modified: Wed, 14 Sep 2022 16:48:09 GMT  
		Size: 80.4 KB (80440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
