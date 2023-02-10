## `openjdk:20-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:9791e9ac979b8592e4ac026167442bae2aacf4f40f3cf921983dfa5ca9dc7dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `openjdk:20-ea-jdk-nanoserver` - windows version 10.0.17763.3887; amd64

```console
$ docker pull openjdk@sha256:c5ff69cad3f3bb8f093c7ba26e40629859432fa5f3d7919db33783203213f4d1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303615343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c96b343e0195dd393259978342a45eda87caf58c30bd669e6bc5e7fd7a2edb46`
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
# Fri, 10 Feb 2023 02:34:50 GMT
ENV JAVA_VERSION=20-ea+35
# Fri, 10 Feb 2023 02:35:08 GMT
COPY dir:bfba2792c6d8d023a0e6075123ea3047c80a5de0ea14d979fe0f656ae5381e0d in C:\openjdk-20 
# Fri, 10 Feb 2023 02:35:56 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 10 Feb 2023 02:35:57 GMT
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
	-	`sha256:381fe7a8a6447ab7dd64c220ca28a708cf469431fb6a7fd772339d6c3a0d97c6`  
		Last Modified: Fri, 10 Feb 2023 08:23:00 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5d8d59fda3be6aa6409e81db16c1c2ed008b701922b8f0c66f03244d7c2097`  
		Last Modified: Fri, 10 Feb 2023 08:23:24 GMT  
		Size: 193.1 MB (193067263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0be3f82c8f1f083ba0fe80b4f6c80fc7b92f244478272605250be036ae046f6`  
		Last Modified: Fri, 10 Feb 2023 08:23:02 GMT  
		Size: 3.8 MB (3804750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a402724dd6b5bd24bfcc601548d91c4148f173fa0de0c6063139d840306453`  
		Last Modified: Fri, 10 Feb 2023 08:23:00 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
