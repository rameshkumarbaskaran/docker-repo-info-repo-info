## `eclipse-temurin:20-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ddc7e81fbb169ed0e4049ab8b8f5969e6768679f551ae78d61d420dcdecb0af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1668; amd64
	-	windows version 10.0.17763.4252; amd64

### `eclipse-temurin:20-jre-nanoserver` - windows version 10.0.20348.1668; amd64

```console
$ docker pull eclipse-temurin@sha256:1a4a8cbca514cbc3abc6e04079ed7ae4a00897d0dd2970db4414f71b527363f2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.2 MB (168231461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f879b350999e08c89e09a95a5cb6c30c062161ee94ef873652c59c6d089ed004`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 12 Apr 2023 01:48:41 GMT
COPY dir:88253b833ff2634324ea23b2cdfd627ca2e30273c5f29426251a8626a4f6baa7 in C:\openjdk-20 
# Wed, 12 Apr 2023 01:48:56 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:19b49903e9ed6af12f9fb83ea522287b16b4c276e34fe96ea7f0e444a9d99083`  
		Last Modified: Wed, 12 Apr 2023 09:48:42 GMT  
		Size: 45.8 MB (45753455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94bb6add05314ed9a1537fa4f48735778aa36cf1b5f6b935a5a90703d57dc47`  
		Last Modified: Wed, 12 Apr 2023 09:48:32 GMT  
		Size: 57.3 KB (57269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:20-jre-nanoserver` - windows version 10.0.17763.4252; amd64

```console
$ docker pull eclipse-temurin@sha256:2307e59c9fe10e9deed4150e8edeeee4f571f32d7a8175354b0d65a1083179eb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155745321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21d098c25075263097966b4bf95bef248bb330b7019ec02df991880a8c25997`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 12 Apr 2023 01:41:56 GMT
COPY dir:88253b833ff2634324ea23b2cdfd627ca2e30273c5f29426251a8626a4f6baa7 in C:\openjdk-20 
# Wed, 12 Apr 2023 01:42:10 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:9e4ce5059d46404cf2912424885d258a872ac13559ba0b0a259e247a5dca94b6`  
		Last Modified: Wed, 12 Apr 2023 09:45:30 GMT  
		Size: 45.7 MB (45738938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cbe07d284b83f45ed7c38496dad4a476250118589c282cbab1400d2bc5e14b`  
		Last Modified: Wed, 12 Apr 2023 09:45:21 GMT  
		Size: 3.1 MB (3142729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
