## `eclipse-temurin:8-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:a89feb254b0ee9e4368f055d9bed44204a4ec9dcb8be8bb55e172bd332c34184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `eclipse-temurin:8-nanoserver-1809` - windows version 10.0.17763.2237; amd64

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
