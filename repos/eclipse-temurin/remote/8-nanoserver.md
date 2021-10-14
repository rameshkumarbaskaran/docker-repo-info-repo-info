## `eclipse-temurin:8-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:fe6ee2a03437fecbdd763783b197cda15f475e445df16d8dcdcad8f783b8175e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.288; amd64
	-	windows version 10.0.17763.2237; amd64

### `eclipse-temurin:8-nanoserver` - windows version 10.0.20348.288; amd64

```console
$ docker pull eclipse-temurin@sha256:dc67e188167c1827151760c3f5ef4708b6e4970db9dbb3622d0ad6f34163df11
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217252719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2cfe7909c5aa05c4feffe06f17d37aae390aaad2a8cfd49dd875847176f111`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Oct 2021 11:15:04 GMT
RUN Apply image ltsc2022-amd64
# Wed, 13 Oct 2021 19:02:30 GMT
SHELL [cmd /s /c]
# Wed, 13 Oct 2021 19:02:31 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Wed, 13 Oct 2021 19:02:32 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Oct 2021 19:02:32 GMT
USER ContainerAdministrator
# Wed, 13 Oct 2021 19:02:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Oct 2021 19:02:49 GMT
USER ContainerUser
# Wed, 13 Oct 2021 19:03:01 GMT
COPY dir:6622177b1379d4d7267ebc9bc4d0bb013ea883bae36028c72b4045f7fa088598 in C:\openjdk-8 
# Wed, 13 Oct 2021 19:03:16 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:91284e7e8fd4bd7ebcfa98544a3e4f59639f38281225c81c34b6fe22e0dba4e5`  
		Size: 116.9 MB (116939483 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ba797e8f93823c3d71c52fcae413f3a33ca28ff2711c09ba5141432948f8298`  
		Last Modified: Wed, 13 Oct 2021 19:43:54 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b013d8b98acd715c3c13d7de9f98d64676bf2486d547545d93a56a2c576fa73`  
		Last Modified: Wed, 13 Oct 2021 19:43:54 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a42ef6fca9ff05407154bf2b7a418a8bd467bfc933bc6581b4047ab17275b46`  
		Last Modified: Wed, 13 Oct 2021 19:43:54 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89143e1acad2a5116c8dbf4a95f6b172d88a5a7eaa294a77716905013b158cff`  
		Last Modified: Wed, 13 Oct 2021 19:43:52 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445a48e48b51c51d06acc0d3d461be030307abf6f59a157ec3de316f1c5261f8`  
		Last Modified: Wed, 13 Oct 2021 19:43:52 GMT  
		Size: 85.8 KB (85779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38acab5055fb1449f4474f91c3cd41b4b22cdbf33ef43143b6e269512e2f85a`  
		Last Modified: Wed, 13 Oct 2021 19:43:52 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7310b71d6fc2a77a0cbb34816abfec40f678cfefad5dc5e365289370eb6dcc8e`  
		Last Modified: Wed, 13 Oct 2021 19:44:03 GMT  
		Size: 100.2 MB (100159858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f9b65f5893706912dc5558a576626b3a62413b4d1ee88feb4417bfedabe7c8`  
		Last Modified: Wed, 13 Oct 2021 19:43:52 GMT  
		Size: 61.8 KB (61776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-nanoserver` - windows version 10.0.17763.2237; amd64

```console
$ docker pull eclipse-temurin@sha256:27cc0866b69c076e7aca0285168fe79d595c6036ff841d6e99780c29ed7836b6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.0 MB (202985871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f512ef8cd4b26f79d64a7d635c2ae973228b6859d264fe9d6e8a8230d8553537`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Oct 2021 08:01:14 GMT
RUN Apply image 1809-amd64
# Wed, 13 Oct 2021 18:17:55 GMT
SHELL [cmd /s /c]
# Wed, 13 Oct 2021 18:17:55 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Wed, 13 Oct 2021 18:17:56 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Oct 2021 18:17:57 GMT
USER ContainerAdministrator
# Wed, 13 Oct 2021 18:18:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Oct 2021 18:18:12 GMT
USER ContainerUser
# Wed, 13 Oct 2021 18:18:25 GMT
COPY dir:6622177b1379d4d7267ebc9bc4d0bb013ea883bae36028c72b4045f7fa088598 in C:\openjdk-8 
# Wed, 13 Oct 2021 18:18:39 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:934e212983f208dc2bebc5de38259a6a62f1761868aacfee2cb3585a13b1e24b`  
		Size: 102.7 MB (102661372 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ceff24c3c0c2c360cd3788fcde5c41e1d6601339f4944623c732558a6030e631`  
		Last Modified: Wed, 13 Oct 2021 19:12:58 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a6866648459c8c90f12126f5b6581327f34b272d63e18f40739e16f778fc46`  
		Last Modified: Wed, 13 Oct 2021 19:12:58 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aac33e066c4d2fa8410826e5d04d739d6d41e991236a94b922cf4ebaf15b715`  
		Last Modified: Wed, 13 Oct 2021 19:12:58 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5c294b63503bb6139aede71e930e77fa4e514c8901a63a6c53e016a7dea26d`  
		Last Modified: Wed, 13 Oct 2021 19:12:56 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ce3f1d3adac21aeff64ee5a834658e889931a8e1479364ec54000d7f8d7ddc`  
		Last Modified: Wed, 13 Oct 2021 19:12:56 GMT  
		Size: 67.5 KB (67464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8151227282ea898d559fd7f4485d14af61dfdc7c83babe26baa15f89630d8856`  
		Last Modified: Wed, 13 Oct 2021 19:12:56 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2459a7d1bccf49eebe8f27a3c9678f4c458d707c9aa3fb2ae503647033704ede`  
		Last Modified: Wed, 13 Oct 2021 19:14:44 GMT  
		Size: 100.2 MB (100160691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1369f102c14d772ac9126d0cca2b91688e9fd91a4a91fa4acf7a2be4e16c56d5`  
		Last Modified: Wed, 13 Oct 2021 19:12:56 GMT  
		Size: 91.1 KB (91051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
