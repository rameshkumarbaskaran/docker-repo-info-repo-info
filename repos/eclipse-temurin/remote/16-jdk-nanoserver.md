## `eclipse-temurin:16-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:88664e4a1bd300960ca371d0d55ff28e1f2ae30f5a01800e5b9c1c17a1353ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `eclipse-temurin:16-jdk-nanoserver` - windows version 10.0.17763.2565; amd64

```console
$ docker pull eclipse-temurin@sha256:ae905d69cb8feecaa6f7d1f69d32b3b04146dc289c06bbfde339582bb50b89db
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305584769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e318abcbd3b283b5e50e476143fe40205ffcbea7895fd96f46f022bf62ea4ad7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:45:32 GMT
SHELL [cmd /s /c]
# Wed, 09 Feb 2022 20:07:34 GMT
ENV JAVA_VERSION=jdk-16.0.2+7
# Wed, 09 Feb 2022 20:07:35 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 09 Feb 2022 20:07:36 GMT
USER ContainerAdministrator
# Wed, 09 Feb 2022 20:07:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Feb 2022 20:07:48 GMT
USER ContainerUser
# Wed, 09 Feb 2022 20:08:24 GMT
COPY dir:9a7ef5975d9ba9576c4744dc049616bbcb218f14c3c0bd967851cd46479d6134 in C:\openjdk-16 
# Wed, 09 Feb 2022 20:08:37 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Feb 2022 20:08:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5a7f567e84a5a148036156650a47ef7eec0187f17e880d3b475e51dacd70077b`  
		Last Modified: Wed, 09 Feb 2022 19:20:50 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a21c9daf457e5d09718f287ef86d24aa0acc087e9a1280321abd00746c0d5d3`  
		Last Modified: Thu, 10 Feb 2022 20:56:35 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b033ab25743d255db793ff7b19754434876b93203f20b029e55dcb3b0514e4f2`  
		Last Modified: Thu, 10 Feb 2022 20:56:35 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b36959d6767f7daa23b3b67552107bba36f06eb4f920599f8c236862bda559`  
		Last Modified: Thu, 10 Feb 2022 20:56:35 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d87f5c9d0b2d97de2b46c15b5f391b4b5af657c995ab38df1ae89d68271f7b`  
		Last Modified: Thu, 10 Feb 2022 20:56:33 GMT  
		Size: 74.0 KB (74020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c475fa4fc6b882ea1d6339f8e39704f185163a434ccf96e9fd5431fc1449477`  
		Last Modified: Thu, 10 Feb 2022 20:56:33 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b008f5f1aa61c085236d0633bd1ed9903a89f43213215efb94670616345d773`  
		Last Modified: Thu, 10 Feb 2022 20:59:57 GMT  
		Size: 198.8 MB (198756397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5cf964d7b859a7eb6abe06db98f3b293cebf11983a04f954c808266d735037`  
		Last Modified: Thu, 10 Feb 2022 20:56:36 GMT  
		Size: 3.7 MB (3660357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3adf44b2a4fac62399b07fb89d787f5619cd2714c9e18d7de21a7acd9af88959`  
		Last Modified: Thu, 10 Feb 2022 20:56:33 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
