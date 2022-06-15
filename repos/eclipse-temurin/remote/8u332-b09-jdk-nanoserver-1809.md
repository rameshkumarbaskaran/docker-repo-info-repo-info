## `eclipse-temurin:8u332-b09-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:750918e2f58b85062623cbae089d745be0a0f5b5a186b54a2fc8de888d8ea968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `eclipse-temurin:8u332-b09-jdk-nanoserver-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull eclipse-temurin@sha256:d62315672fa3d22ab6a60f7b36fb1a5d1a1a47828e769c81d2a0358941370fb0
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203383199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44b681a89064f30727eba32a0134e2c9cafc1cadcdaffeec3b980311e465ee8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jun 2022 19:20:11 GMT
RUN Apply image 10.0.17763.3046
# Wed, 15 Jun 2022 17:30:58 GMT
SHELL [cmd /s /c]
# Wed, 15 Jun 2022 17:30:59 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Wed, 15 Jun 2022 17:31:00 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Jun 2022 17:31:01 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 17:31:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jun 2022 17:31:18 GMT
USER ContainerUser
# Wed, 15 Jun 2022 17:31:30 GMT
COPY dir:fe4a23cbc3aecb3ea1bcf0dca600117ebc14653b599151b614599054d6b82722 in C:\openjdk-8 
# Wed, 15 Jun 2022 17:31:46 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:d555a7e4de4dd775379d5c43c1419374bff7908670dc7444be5e8e8f386f3d26`  
		Size: 103.2 MB (103153235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92b4c385cd5cbb12fb09cb31c12b5e5de38cf7b380c8681286caac242c06d3ed`  
		Last Modified: Wed, 15 Jun 2022 18:22:11 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8383a858caadd7c08d904c28b46f27e089462aa2a5d850bd015b1c1fbf329d`  
		Last Modified: Wed, 15 Jun 2022 18:22:10 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6f169c62581740c10d7cd192d43505ba7a73aa0afb6ea2eef4d677002028f6`  
		Last Modified: Wed, 15 Jun 2022 18:22:11 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbc6e2437dffe104ee945cec068774854fc9adab78010af3a744b81edfd1b79`  
		Last Modified: Wed, 15 Jun 2022 18:22:08 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528ebce201545bb21af7fa54da27a6431bfe29f84732f039098454a7e505f42e`  
		Last Modified: Wed, 15 Jun 2022 18:22:08 GMT  
		Size: 68.4 KB (68380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b918f70d4abdc14639224ba8a620508a5a7e3d1cccfc1bbd60ebd35f2a763a8`  
		Last Modified: Wed, 15 Jun 2022 18:22:08 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c624f82ec5e39d75726a36b9182daf77982c4fb9762300266a80f3ba172a907`  
		Last Modified: Wed, 15 Jun 2022 18:23:57 GMT  
		Size: 100.1 MB (100073978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a1cd5ecfd32fe9a25d3c54bc2047320e5efd1efc261dff847cf6aaef0befcc`  
		Last Modified: Wed, 15 Jun 2022 18:22:08 GMT  
		Size: 81.7 KB (81734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
