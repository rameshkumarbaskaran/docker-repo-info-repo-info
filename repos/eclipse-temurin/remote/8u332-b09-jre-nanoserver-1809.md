## `eclipse-temurin:8u332-b09-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:3be0a909fb6f5e81fd59c590c4bc3d04a52026f9b5e1e3371d1e60a7b40acb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `eclipse-temurin:8u332-b09-jre-nanoserver-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull eclipse-temurin@sha256:5bd0c4ff5185d7b95c386ce29cc1293026cc8d50bef663c198487a6518f45834
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142454341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d5e43d575d959d4efc4754b8c2732d14b8bc552b70453da608ebf49c5e8f7b`
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
# Wed, 15 Jun 2022 17:35:48 GMT
COPY dir:3ac3da968b0a55dd3b56d678ae78ff2fe7435f143b42a50fa75d097fd864892f in C:\openjdk-8 
# Wed, 15 Jun 2022 17:36:01 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:daaad8e234c604da65f3a9232bef4adf372995e59d3671dc64ce43cc79e9bc07`  
		Last Modified: Wed, 15 Jun 2022 18:27:43 GMT  
		Size: 39.1 MB (39145796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada199130844990dbcfa73e236c31d26f73a7a0a69cd6a44a03e1f6e3628acfd`  
		Last Modified: Wed, 15 Jun 2022 18:27:02 GMT  
		Size: 81.1 KB (81058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
