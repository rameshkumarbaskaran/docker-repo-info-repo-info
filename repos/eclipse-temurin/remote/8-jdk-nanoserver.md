## `eclipse-temurin:8-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ca5e232868f99d54dc2cd69c830a8f4a3be170ae3cc168fc4688cefed1f7ba5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:b568f82f81d91991a31430ef408475e93b7ac18d7e402bde8855c014533f2a48
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218758228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5971e02317165e2357b29fc38786fc28298bcd28190232df35a8b78c77828078`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Sep 2022 20:11:22 GMT
RUN Apply image 10.0.20348.1006
# Wed, 14 Sep 2022 16:38:20 GMT
SHELL [cmd /s /c]
# Wed, 14 Sep 2022 16:38:21 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Wed, 14 Sep 2022 16:38:21 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 Sep 2022 16:38:22 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 16:38:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Sep 2022 16:38:37 GMT
USER ContainerUser
# Wed, 14 Sep 2022 16:38:48 GMT
COPY dir:3f2d3aa63ba7a56176deaae1ba1b26dbdbe105074828954c77b0da527aacd6d7 in C:\openjdk-8 
# Wed, 14 Sep 2022 16:39:03 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:09629875cd6ee57fa551626fa2963d8b54718ba9acbf28e7cb5d684a9cb754d7`  
		Size: 118.1 MB (118131331 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:07f30e2ceaa03f6ac7b6e6f319083288f48d1fa2a61f36f51f516da241496976`  
		Last Modified: Wed, 14 Sep 2022 16:57:28 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16323d7400627da10ce240f6e16c64f6ede4747acabd111c1f97f3ad620293ec`  
		Last Modified: Wed, 14 Sep 2022 16:57:29 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002ad03790aa608a5e569e2bb5524ab646f494ff6129d26716ae8b523a371076`  
		Last Modified: Wed, 14 Sep 2022 16:57:28 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15108493c7dc7578b06d64ea9a5472d2f923e209c7e0342954ba5f5de11379d`  
		Last Modified: Wed, 14 Sep 2022 16:57:26 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4b7ee065d4dfbef0b4508eb703bf0abaddfa3a39bdce741b72f9c1c1fa1e1c`  
		Last Modified: Wed, 14 Sep 2022 16:57:26 GMT  
		Size: 79.6 KB (79618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266593abc7831b07aa3367c5799233affe80baa3691fb02ec3f9207a5403d4d1`  
		Last Modified: Wed, 14 Sep 2022 16:57:26 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4a834df7059a1e2e704b02ea037d3a52f17963bcfd3314ae1933d426985f78`  
		Last Modified: Wed, 14 Sep 2022 16:57:38 GMT  
		Size: 100.5 MB (100480177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa21228b73836d634eeb540ae7f49a67603435e1280387e244ba1c0420068e23`  
		Last Modified: Wed, 14 Sep 2022 16:57:26 GMT  
		Size: 62.0 KB (61961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.17763.3406; amd64

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
