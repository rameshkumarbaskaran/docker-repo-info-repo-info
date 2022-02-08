## `openjdk:19-ea-8-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:9775469bafa22d6edfeb5628b6075704a80dcd63b6aa660312036318d06188de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `openjdk:19-ea-8-jdk-nanoserver` - windows version 10.0.17763.2458; amd64

```console
$ docker pull openjdk@sha256:59470b233cff183d75794b975fedaf3ae19e7d8e7925ceb9e8f541f47e94c865
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.6 MB (291599556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6438fabf47ef9e5786f74cbb9ba6b82c19f52e38327452eb75f94034d29389e2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 19 Jan 2022 22:25:45 GMT
SHELL [cmd /s /c]
# Wed, 19 Jan 2022 22:25:45 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 19 Jan 2022 22:25:46 GMT
USER ContainerAdministrator
# Wed, 19 Jan 2022 22:25:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 19 Jan 2022 22:26:00 GMT
USER ContainerUser
# Tue, 08 Feb 2022 02:20:11 GMT
ENV JAVA_VERSION=19-ea+8
# Tue, 08 Feb 2022 02:20:44 GMT
COPY dir:085c70939dba172f061bec7e04a177fe07855c76d2d86340a67635a03ecbe2d1 in C:\openjdk-19 
# Tue, 08 Feb 2022 02:21:00 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 08 Feb 2022 02:21:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a1b3e13bb7b3d4b61b5f49a91d6eb9bfcf5539ab89c3687d608f17713c2409b5`  
		Last Modified: Thu, 20 Jan 2022 02:21:30 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37e2d9d248af5cc77da02f6689e73057a6b209b1e2cc18d237e2225251d508c`  
		Last Modified: Thu, 20 Jan 2022 02:21:30 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a757e837e961d995033dd26e4129e5adf88e7675118d83eb95cfccdd2f5170`  
		Last Modified: Thu, 20 Jan 2022 02:21:30 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8711fe31967a4951c1345f1b126afe50ed968967c304e43d8e05224db1186e7f`  
		Last Modified: Thu, 20 Jan 2022 02:21:29 GMT  
		Size: 72.5 KB (72539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0481682eb573fcc3023c5291f96696ee373749cac12ceec16c1f2a990b142e78`  
		Last Modified: Thu, 20 Jan 2022 02:21:27 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9060af5c56d9c214900055f0d8117030e616dab6301b88ab2d3e9ba7e6c462`  
		Last Modified: Tue, 08 Feb 2022 03:28:23 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9f53230d35c9340224cea0c56fa7ef5f48a1781968aa84c82bacce1ea2d51c`  
		Last Modified: Tue, 08 Feb 2022 03:31:35 GMT  
		Size: 185.0 MB (184960529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c660a4869b017a61baded9ea71fd7dd620a2f5858d0349154ebf023c1af7d3e0`  
		Last Modified: Tue, 08 Feb 2022 03:28:26 GMT  
		Size: 3.5 MB (3513023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d257508857b48a2091c387f3392340e5dc922b1b5a64378ed073e25794994f36`  
		Last Modified: Tue, 08 Feb 2022 03:28:23 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
