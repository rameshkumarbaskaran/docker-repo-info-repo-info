## `eclipse-temurin:8-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:4939bd33048a256e525f7af68e283c7bf6f5ba676b1e0c3322a78c0175b54969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `eclipse-temurin:8-jdk-nanoserver-1809` - windows version 10.0.17763.4252; amd64

```console
$ docker pull eclipse-temurin@sha256:282f8b2ca40d90c89bdc056513ea1b471ea405d97f2e7b81b82c3e3064f0d30d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208375728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1eb09d33ae0944db9b94f7db2eaf2401930f762bbcca2ac83371b9c88e641a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Tue, 11 Apr 2023 23:45:41 GMT
SHELL [cmd /s /c]
# Wed, 12 Apr 2023 01:00:37 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 12 Apr 2023 01:00:38 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Apr 2023 01:00:39 GMT
USER ContainerAdministrator
# Wed, 12 Apr 2023 01:00:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Apr 2023 01:00:54 GMT
USER ContainerUser
# Wed, 12 Apr 2023 01:01:05 GMT
COPY dir:8214f6b15a617bff549fa1e8e973ad9cf58dcd41804c9c4d00b4aebf5303ecc4 in C:\openjdk-8 
# Wed, 12 Apr 2023 01:01:40 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:af799fb2ff133c89311c6a42d34b8cb6c9b11d775f52e04ab08389d05e64ed1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:10 GMT  
		Size: 106.8 MB (106788951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1db438f20b81fe0c031e4e3eee58d278fba7258d01057ff18964cccf70d41c`  
		Last Modified: Wed, 12 Apr 2023 00:52:38 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5593d7ff65e071c973825c7d57969b7431518490174383b2cc83b5272296d69`  
		Last Modified: Wed, 12 Apr 2023 09:35:19 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da43b0e68ac3ed536edc3110c6c369d90f6c8ce83d22fd01c21b77883982994`  
		Last Modified: Wed, 12 Apr 2023 09:35:19 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5798c8a6554f2ad678b5090d67918fc66af0fa922dc37577a0c3c135241264d4`  
		Last Modified: Wed, 12 Apr 2023 09:35:17 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda7d4d02f9e02ded3b5495fee94a3bf6dfaad7271d7fb26f996d061ac4747c4`  
		Last Modified: Wed, 12 Apr 2023 09:35:17 GMT  
		Size: 77.7 KB (77691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dacb99131be332bd145d4ed8040f668d972a74e3bc970e43283fdf3d6f61deb`  
		Last Modified: Wed, 12 Apr 2023 09:35:17 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80d2496ce3b986aef76755085fdc9874ecdfcde74d6c0e2afaee8ae5c34a732`  
		Last Modified: Wed, 12 Apr 2023 09:35:31 GMT  
		Size: 101.4 MB (101416306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf53175bf956afa22b6b8611d790be239da28aa4c585c7d03b188151cbbfea`  
		Last Modified: Wed, 12 Apr 2023 09:35:17 GMT  
		Size: 87.0 KB (86980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
