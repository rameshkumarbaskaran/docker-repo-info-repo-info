## `eclipse-temurin:20-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:79bc0e41810c694991b763c262452fa487e0802e53e83289a8fe0ab631c22183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1668; amd64
	-	windows version 10.0.17763.4252; amd64

### `eclipse-temurin:20-jdk-nanoserver` - windows version 10.0.20348.1668; amd64

```console
$ docker pull eclipse-temurin@sha256:a69c7e62cb3b6327eab70ff091596475b4fdd12e569f2ad760a16dc2f263f185
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.7 MB (317736810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c56bb0445eef2d4b58f353d1c9c0ffc7c1bc8b2aaba4afa76fffc52cd00719`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:16 GMT
RUN Apply image 10.0.20348.1668
# Wed, 12 Apr 2023 01:42:21 GMT
SHELL [cmd /s /c]
# Wed, 12 Apr 2023 01:47:28 GMT
ENV JAVA_VERSION=jdk-20+36
# Wed, 12 Apr 2023 01:47:29 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 12 Apr 2023 01:47:29 GMT
USER ContainerAdministrator
# Wed, 12 Apr 2023 01:47:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Apr 2023 01:47:40 GMT
USER ContainerUser
# Wed, 12 Apr 2023 01:47:56 GMT
COPY dir:0bba24b8a26333fabbf995368b29d05051d1ff1f33d04d60afd33310da1fd9b4 in C:\openjdk-20 
# Wed, 12 Apr 2023 01:48:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Apr 2023 01:48:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e06b772d586b58466a653b72002aee7c59496110e9ae402ff58f026e44452506`  
		Last Modified: Wed, 12 Apr 2023 02:34:14 GMT  
		Size: 122.3 MB (122328782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8058ec80ac2516d001291dea383d4abfa22416397a4c869e6fd79c0d4b64565f`  
		Last Modified: Wed, 12 Apr 2023 09:45:40 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d771ecdf092529e0c97bd1e4f0a478bf6923159b17d1650d091f062627e215c7`  
		Last Modified: Wed, 12 Apr 2023 09:47:58 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c60e8241e702088dc2ffcc30dc7902f7e53ae5f0e7b203b03811dff7ce9684`  
		Last Modified: Wed, 12 Apr 2023 09:47:57 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784c970ac0afccfe355779fa5ead00807dda21bf87b1faf2ff0fa8a9cfae3d76`  
		Last Modified: Wed, 12 Apr 2023 09:47:57 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5061be6624f789f71935eaf2a00de889b24c06e42f237d96b99e3cb720d2086`  
		Last Modified: Wed, 12 Apr 2023 09:47:56 GMT  
		Size: 86.6 KB (86612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0da7e587c56006cb75a21efef088296fcbb73f6c2a2cf780b8baf4f2144dfd`  
		Last Modified: Wed, 12 Apr 2023 09:47:55 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbab285f9a15b8338c2cbb45532b1836ccb5a66718f1796e6ed303b4f56457a`  
		Last Modified: Wed, 12 Apr 2023 09:48:20 GMT  
		Size: 195.2 MB (195241477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5ccfdcd850e7a0f71861f94d95933ac88ddb5656b64410f293efbaba20faff`  
		Last Modified: Wed, 12 Apr 2023 09:47:56 GMT  
		Size: 73.5 KB (73466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9a02e18ef9e60ac3cf787af4eb5a20e4ab9a77390a624c05a66ca3e20aee13`  
		Last Modified: Wed, 12 Apr 2023 09:47:55 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:20-jdk-nanoserver` - windows version 10.0.17763.4252; amd64

```console
$ docker pull eclipse-temurin@sha256:25afa3e785c7350c2daf7b4e732cc4951618cafc3d11a8e04fafb46d63b019b3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305895501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec55d7ed4409db5456aa35d0b03253f129132a0ff317257f40a418efc0194ab`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Tue, 11 Apr 2023 23:45:41 GMT
SHELL [cmd /s /c]
# Wed, 12 Apr 2023 01:36:30 GMT
ENV JAVA_VERSION=jdk-20+36
# Wed, 12 Apr 2023 01:36:31 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 12 Apr 2023 01:36:31 GMT
USER ContainerAdministrator
# Wed, 12 Apr 2023 01:36:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Apr 2023 01:36:49 GMT
USER ContainerUser
# Wed, 12 Apr 2023 01:37:04 GMT
COPY dir:0bba24b8a26333fabbf995368b29d05051d1ff1f33d04d60afd33310da1fd9b4 in C:\openjdk-20 
# Wed, 12 Apr 2023 01:37:25 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Apr 2023 01:37:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af799fb2ff133c89311c6a42d34b8cb6c9b11d775f52e04ab08389d05e64ed1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:10 GMT  
		Size: 106.8 MB (106788951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1db438f20b81fe0c031e4e3eee58d278fba7258d01057ff18964cccf70d41c`  
		Last Modified: Wed, 12 Apr 2023 00:52:38 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ce5de1c6c3e182e390fbd587888ada347a6c8acdb9c36d0acb82b56f58f723`  
		Last Modified: Wed, 12 Apr 2023 09:44:06 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2176ad1b2d01a0c49cfafd513e39dfdcb902e1434a6575bf7d726c547e71a3`  
		Last Modified: Wed, 12 Apr 2023 09:44:05 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa7cd546e7dbbb9155483c115c8a501d58faf398c62d3162d3b631972d27d00`  
		Last Modified: Wed, 12 Apr 2023 09:44:05 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75552b77c71ecbb7dba9a11bfc508d63227ea66c2866e7c061a8885537ad56f`  
		Last Modified: Wed, 12 Apr 2023 09:44:04 GMT  
		Size: 69.0 KB (69018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdaa54362a8c4616f7807a0e03039c0d746f0118e5de1c97a087c723978ec78`  
		Last Modified: Wed, 12 Apr 2023 09:44:03 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c51129b872081d27401412f8a4cbd71d69552ddd07f826aa2206661429a7db`  
		Last Modified: Wed, 12 Apr 2023 09:44:26 GMT  
		Size: 195.3 MB (195253749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7569653c69e88f355755b234f886cdc59e31a9886cbdcc934b2495285281520c`  
		Last Modified: Wed, 12 Apr 2023 09:44:04 GMT  
		Size: 3.8 MB (3776958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c143b76a080e1768638485ee1f8710964f0dad6f4631c26127b93442c00417e`  
		Last Modified: Wed, 12 Apr 2023 09:44:03 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
