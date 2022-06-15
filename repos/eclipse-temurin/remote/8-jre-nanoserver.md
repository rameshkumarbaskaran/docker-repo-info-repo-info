## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:b187d0653ab2aa6eb8c2076a659e924c7a9bb888e5b9943c0e74a61ce63f6675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.768; amd64
	-	windows version 10.0.17763.3046; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.768; amd64

```console
$ docker pull eclipse-temurin@sha256:ac83b262ca86be800452eacb73384f7a0bcc8c52359db5ea1b36d0d55f1e8eea
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157256052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23cf120e0867f735ec1b95d0a6829a0dd99a4f3cfa0b4a60051e0add9cbaec3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jun 2022 04:10:14 GMT
RUN Apply image 10.0.20348.768
# Wed, 15 Jun 2022 18:08:52 GMT
SHELL [cmd /s /c]
# Wed, 15 Jun 2022 18:08:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Wed, 15 Jun 2022 18:08:54 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Jun 2022 18:08:55 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 18:09:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jun 2022 18:09:27 GMT
USER ContainerUser
# Wed, 15 Jun 2022 18:10:11 GMT
COPY dir:3ac3da968b0a55dd3b56d678ae78ff2fe7435f143b42a50fa75d097fd864892f in C:\openjdk-8 
# Wed, 15 Jun 2022 18:10:26 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:fca88290e1b048d74ec4e9d1548c4ec09dc3921f80285f39a186278fcaf2d86f`  
		Size: 118.0 MB (117976537 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:60cbdb7704dc53714205f32082d3faa20d7c93a53c40cb88f22581e85a2943fc`  
		Last Modified: Wed, 15 Jun 2022 19:13:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b9c7257f423af50da401b2650d6841549dbd95f433b8bb78423f42558cf255`  
		Last Modified: Wed, 15 Jun 2022 19:13:51 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5306ed3ad268c7fefb13d64b3f2cd6ee35898cd2bffb428b6e1c2aa20399568b`  
		Last Modified: Wed, 15 Jun 2022 19:13:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf5d1ee027f5de50fd4b2a177fd62b473a0c007c38d86ed1aca48cdde03b8cf`  
		Last Modified: Wed, 15 Jun 2022 19:13:44 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26734ec0ceb29a842317ce27bd3cdc7fac47ba4055a0b5f3d84d283a318f0f43`  
		Last Modified: Wed, 15 Jun 2022 19:13:44 GMT  
		Size: 86.7 KB (86727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdfe0c7bc62a1f4b9cecfbc56d7f04f29a4788cfb900e246605e476ac500bff`  
		Last Modified: Wed, 15 Jun 2022 19:13:44 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9de885c91e2ded6d3ea581d750c8cee2d4a66e40b1ce39dc5cf9655518ec0e`  
		Last Modified: Wed, 15 Jun 2022 19:16:26 GMT  
		Size: 39.1 MB (39128560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7202f88991e8bd827e33a6850ebdd754b78dd5f5f385ab984fd514ad7cdfb41`  
		Last Modified: Wed, 15 Jun 2022 19:15:45 GMT  
		Size: 58.4 KB (58387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.17763.3046; amd64

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
