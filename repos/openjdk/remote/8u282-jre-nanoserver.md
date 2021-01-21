## `openjdk:8u282-jre-nanoserver`

```console
$ docker pull openjdk@sha256:94cbcd3f563fd873e19f299a4d0aa8a50b93167ac3e7f2622bf3346aa8656edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:8u282-jre-nanoserver` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:7b0bb1771204087be242e21b6def8617f9ecb5bfaaf946631100da762e7ce091
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139688383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5375ee0b962c2dc89b2794250e2d9aa86d4fdf5954e2b8b15d80a1283dca5cd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:56:48 GMT
SHELL [cmd /s /c]
# Wed, 13 Jan 2021 21:01:53 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Jan 2021 21:01:54 GMT
USER ContainerAdministrator
# Wed, 13 Jan 2021 21:02:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 13 Jan 2021 21:02:06 GMT
USER ContainerUser
# Thu, 21 Jan 2021 02:28:33 GMT
ENV JAVA_VERSION=8u282
# Thu, 21 Jan 2021 02:32:29 GMT
COPY dir:f51b6315789fea62bc81073100310d85cf4082234fc7f3bd9b51f6f4a883a8f3 in C:\openjdk-8 
# Thu, 21 Jan 2021 02:32:40 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c2b6c001c337f812bceb3b03d15a70d1d9905540658e751e42f20f7cc0ddc819`  
		Last Modified: Wed, 13 Jan 2021 21:16:47 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eb6e28c3ff306f6c33045aed2e65fcab8f045964fdf585fd9ff1a04fb6f4f1`  
		Last Modified: Wed, 13 Jan 2021 21:40:49 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9732ca3e0c38e5c843b184efac598a5a240580f63845fd6d6785d74beb864c5a`  
		Last Modified: Wed, 13 Jan 2021 21:40:48 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f226704d058e27f81a0b344cc0c09c4c8e2604ae02105ee61981cec67ee74c`  
		Last Modified: Wed, 13 Jan 2021 21:40:46 GMT  
		Size: 64.9 KB (64879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba37b590809af3c8a52b218cd2c383b7017b5628bcba2e0290e0d379dc2404c`  
		Last Modified: Wed, 13 Jan 2021 21:40:45 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc2fc16e463968ba0f00e322f83fc0819e7f06bf947cea8f7d2c52ac625316b`  
		Last Modified: Thu, 21 Jan 2021 02:46:21 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e6acb8654ea7fe380cd4aa33f20d899ccb2ec84f79419f8f0833ab6d579c28`  
		Last Modified: Thu, 21 Jan 2021 02:49:28 GMT  
		Size: 38.2 MB (38198654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e636174d9ec36847d4fdb21632d6a244a2aa6f2a74081b81efe96371c0bf97e`  
		Last Modified: Thu, 21 Jan 2021 02:49:20 GMT  
		Size: 80.2 KB (80189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
