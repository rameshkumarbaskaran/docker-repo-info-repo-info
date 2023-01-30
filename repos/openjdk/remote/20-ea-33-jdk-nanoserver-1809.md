## `openjdk:20-ea-33-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:88f81ece00d15d8f57269c38cc03f2c578750f2c31490862de17a4961ab9a78b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `openjdk:20-ea-33-jdk-nanoserver-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull openjdk@sha256:9b3e259b135940b48e55c0cfbb2300111d371c1237df8fadd79d5d6ec7834367
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303603418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fa0e7783585bd7a58fa912eb72a61284118f3cce98381e09e11e07e094428b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jan 2023 05:17:01 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:45:31 GMT
SHELL [cmd /s /c]
# Thu, 12 Jan 2023 05:15:32 GMT
ENV JAVA_HOME=C:\openjdk-20
# Thu, 12 Jan 2023 05:15:33 GMT
USER ContainerAdministrator
# Thu, 12 Jan 2023 05:15:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 12 Jan 2023 05:15:43 GMT
USER ContainerUser
# Mon, 30 Jan 2023 19:23:08 GMT
ENV JAVA_VERSION=20-ea+33
# Mon, 30 Jan 2023 19:23:27 GMT
COPY dir:e2c96f8cd986179d1aed482d6af45bb1bf14deec87d736ac2e41321a53bee49e in C:\openjdk-20 
# Mon, 30 Jan 2023 19:23:59 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 30 Jan 2023 19:23:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e58f9ad3b15a2a4882ab0a845e8e619cc8c3c411ddbe8b50046c1618a95c1397`  
		Last Modified: Thu, 12 Jan 2023 02:40:44 GMT  
		Size: 106.7 MB (106666138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea67a6bd980bdee35399883e5abcc31c738b338ad384b2f92d91a15cf09d9df`  
		Last Modified: Thu, 12 Jan 2023 02:40:16 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96518e54215f38193b505640cdb2fef097c5741e65b4b97bba8f867e243d032`  
		Last Modified: Thu, 12 Jan 2023 05:25:44 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d63c92ba435f57ba529ea551f43866f6d4eba3a81d296b0fb044c740f2ee807`  
		Last Modified: Thu, 12 Jan 2023 05:25:44 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b356ba1f31bf25142c630cbcb07b081461c3f630e690d98dc24ae4786a9ef7a`  
		Last Modified: Thu, 12 Jan 2023 05:25:44 GMT  
		Size: 70.5 KB (70518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638383fe215678a48f17d26ca2a40f4c79f0e0929d53790d7d9d5d1d73cdb9cb`  
		Last Modified: Thu, 12 Jan 2023 05:25:42 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63936a380e6ed470e1f18e6327c9e13bb6a01a07656f5adfeae4c5cc98803b5f`  
		Last Modified: Mon, 30 Jan 2023 19:30:07 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1cce2d22f2e5dab8055d31617b1cc7c7151d886efceb7a667cf6daf9060209`  
		Last Modified: Mon, 30 Jan 2023 19:30:31 GMT  
		Size: 193.1 MB (193068263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0ba2110f0a34dbcdd49e3fcfa446ba768a1d40df3059c65c57d05e0a99b7fd`  
		Last Modified: Mon, 30 Jan 2023 19:30:08 GMT  
		Size: 3.8 MB (3791796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d12b0dcdfdba3e7eed0c01a940bb843aa1b9a6c4e523e3123828dfc03dbb6b`  
		Last Modified: Mon, 30 Jan 2023 19:30:07 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
