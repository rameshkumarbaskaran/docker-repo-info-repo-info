## `openjdk:8-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:666397cfa02316e923215c0763f6e136c6b2e120f6d0c2e58c808440e9ca7ad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:8-jdk-nanoserver-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:107b294f967ab5da5da80d3917483b138c1a49a12573ba131f4dd4bb61c72947
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.5 MB (202488052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ecf47773c8eba0a88df00360a2676332225ac92489033a1cda4c3ad8ca5ea5`
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
# Thu, 21 Jan 2021 02:28:55 GMT
COPY dir:6f6bc9ea1f93ff1db59b5fd63225d3a5b1df7d373dee2c520410df56c408f0e1 in C:\openjdk-8 
# Thu, 21 Jan 2021 02:29:08 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version
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
	-	`sha256:dc36730f77e08e8482ad5e9d1f372222be8f377c06dc8edd8d84fc27cfb9956c`  
		Last Modified: Thu, 21 Jan 2021 02:48:11 GMT  
		Size: 101.0 MB (100989380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf16d37bfa9ada8df69e2d16a83d82ac769328f3491e34f400b9d9f8aaa8c5b1`  
		Last Modified: Thu, 21 Jan 2021 02:46:21 GMT  
		Size: 89.1 KB (89132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
