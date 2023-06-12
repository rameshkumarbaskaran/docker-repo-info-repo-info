## `openjdk:22-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:fedcac825e97b8b42cfc470d9bee7c052ee02409c4b44b38a4341e421fef877a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `openjdk:22-ea-jdk-nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull openjdk@sha256:e98cda0869c644ca84575008d228bf9fe8446b3f6fc26b5c3536c489cec0c381
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307110271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0ae67708bf98c78b0501e03af1d1f5b8c6f4233afa5ce9693d00efc728a6d1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 00:40:01 GMT
SHELL [cmd /s /c]
# Mon, 12 Jun 2023 22:19:44 GMT
ENV JAVA_HOME=C:\openjdk-22
# Mon, 12 Jun 2023 22:19:44 GMT
USER ContainerAdministrator
# Mon, 12 Jun 2023 22:19:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 12 Jun 2023 22:19:55 GMT
USER ContainerUser
# Mon, 12 Jun 2023 22:19:55 GMT
ENV JAVA_VERSION=22-ea+1
# Mon, 12 Jun 2023 22:20:10 GMT
COPY dir:b92259b80436bb1fd33a07a598f496a2bb18bd238b995c9b8b4c25abf0b81a2d in C:\openjdk-22 
# Mon, 12 Jun 2023 22:20:24 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 12 Jun 2023 22:20:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b79dd15c5dd82bc10521b9a4e49241f70088bc6edbb286f90be198abea55e23`  
		Last Modified: Wed, 10 May 2023 03:01:27 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3175287b6f32a6af67d4dd84cf40b35af069fc23b52be5b8681182c7784bcd47`  
		Last Modified: Mon, 12 Jun 2023 22:23:13 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a46f3af19909da91109425dda44628673a5784c816b38f3c3d3c5018303e421`  
		Last Modified: Mon, 12 Jun 2023 22:23:13 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba59b819496b185d571623e576a7f3f4d9140857c5e1483bf8ecd7a687bf3dba`  
		Last Modified: Mon, 12 Jun 2023 22:23:13 GMT  
		Size: 67.3 KB (67268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025ffd586aebd9aa36149eec02248b6e27e8bd8d12d2d7f9ed3da24c282b2d39`  
		Last Modified: Mon, 12 Jun 2023 22:23:11 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eef053ffe1a74c3632770bd28fa5ae0debd2f8e9a31c1e23cf5b21629b4c696`  
		Last Modified: Mon, 12 Jun 2023 22:23:11 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a6be05865c90de9b6d2871a1c34ef4ec00897e7aae589687731756584d7f29`  
		Last Modified: Mon, 12 Jun 2023 22:23:30 GMT  
		Size: 198.8 MB (198842210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c442358869efb1569e7f9220f28052053ad3a259329f4d56e53a84afc6a9fa94`  
		Last Modified: Mon, 12 Jun 2023 22:23:12 GMT  
		Size: 3.8 MB (3809864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f991b18e84dbd5549f375b8cfcbef5e64c6148316f696a969525e8772ac55f`  
		Last Modified: Mon, 12 Jun 2023 22:23:11 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
