## `openjdk:18-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:341e0d57656c03b1d7e0c94ec7a6b5868effa3f74976e5658a1ea9cb00a5d266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `openjdk:18-jdk-nanoserver-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull openjdk@sha256:bbe3656b31f6c8304ac49be4312961373e6813816ae4e751e2d21f2904ac2ca4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.7 MB (290652001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6580530b9219c126f2ba77296ad5ea3381d616609394b8757d65d3067897109`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 19 Jan 2022 22:25:45 GMT
SHELL [cmd /s /c]
# Wed, 19 Jan 2022 22:28:51 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 19 Jan 2022 22:28:52 GMT
USER ContainerAdministrator
# Wed, 19 Jan 2022 22:29:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 19 Jan 2022 22:29:07 GMT
USER ContainerUser
# Wed, 19 Jan 2022 22:29:08 GMT
ENV JAVA_VERSION=18-ea+31
# Wed, 19 Jan 2022 22:29:36 GMT
COPY dir:1d6cd53539900778f39da02e3bae89311582b4a1022ea14259be995dc157af87 in C:\openjdk-18 
# Wed, 19 Jan 2022 22:29:53 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 19 Jan 2022 22:29:54 GMT
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
	-	`sha256:848f0583ef29156642246562456f8e070e665d934ee5b5eca5da3a549c83b769`  
		Last Modified: Thu, 20 Jan 2022 02:26:27 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e408e60a5374b05b851d28c9154c5da23c66b31ff9344a9d4aa29e471f89a90f`  
		Last Modified: Thu, 20 Jan 2022 02:26:27 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fd9cc1e1a14cc04328a97d502fe56af7c5256437bad3c9c13e77832c28f28e`  
		Last Modified: Thu, 20 Jan 2022 02:26:27 GMT  
		Size: 68.6 KB (68587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cd88d42425b3a9d8b74a22ca8c7ca9daaa1903b0a06ee4fd2194cd5acf6362`  
		Last Modified: Thu, 20 Jan 2022 02:26:25 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c40ed9b3c2a32eadd9a310b1a7ddb748081f087dd192ef97100c9ca6c93844`  
		Last Modified: Thu, 20 Jan 2022 02:26:25 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e50e246849d1b8bb731fbd5fc84245d920c88e46f6debc8fb0b73734cab6dad`  
		Last Modified: Thu, 20 Jan 2022 02:26:49 GMT  
		Size: 184.0 MB (183981774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea21550029dcc1d95a18cd1bc12d7df50c4dfeab3b0699017c25f225dd93f89`  
		Last Modified: Thu, 20 Jan 2022 02:26:26 GMT  
		Size: 3.5 MB (3548193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290aa5602576bcfe5a0e440ea21bcd0dba7f995cec222f1dbf063fe05bbe3291`  
		Last Modified: Thu, 20 Jan 2022 02:26:24 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
