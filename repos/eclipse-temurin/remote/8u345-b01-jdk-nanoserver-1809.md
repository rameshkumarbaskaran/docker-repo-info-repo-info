## `eclipse-temurin:8u345-b01-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:d3a7e2311684f997d4f70a6f19e76b29ec63945749ebc43cc7144394226bb026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:8u345-b01-jdk-nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull eclipse-temurin@sha256:e6de518116942087b5b8c14a8f3521925354e68bf56696939e07e35a0bc400d2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (203967382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d6d1c0eae8e50e8634f713fb2d9a93055b3e24793907c0bc42afb376a02f98`
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
# Wed, 14 Sep 2022 16:03:27 GMT
COPY dir:3f2d3aa63ba7a56176deaae1ba1b26dbdbe105074828954c77b0da527aacd6d7 in C:\openjdk-8 
# Wed, 14 Sep 2022 16:03:43 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:8220133522d11b0ce2a7e89fe5f6e5ff8d879b5ef86ae84dc14de0ed55988aa3`  
		Last Modified: Wed, 14 Sep 2022 16:47:21 GMT  
		Size: 100.5 MB (100469504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57384d93677ab30125b868d44f5bd6294a0d20ed7ef721062585a3349929143`  
		Last Modified: Wed, 14 Sep 2022 16:47:09 GMT  
		Size: 90.2 KB (90224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
