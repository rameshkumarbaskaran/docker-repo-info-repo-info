## `eclipse-temurin:8-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:aa2656ec26f15bf051f8cb20e76f14f1bbb4f9f01a077d9698d4a830d34cacd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1668; amd64

### `eclipse-temurin:8-nanoserver-ltsc2022` - windows version 10.0.20348.1668; amd64

```console
$ docker pull eclipse-temurin@sha256:8e64fc5e9619d1c3e989daf13d39d36b08226fc95b7c4c1915f7b335c1c83ae6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223912081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6651a0e4ba820a84d30ed4e8d4f7361f51d79715a36e54b011b39ccf1fdcf250`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:16 GMT
RUN Apply image 10.0.20348.1668
# Wed, 12 Apr 2023 01:42:21 GMT
SHELL [cmd /s /c]
# Wed, 12 Apr 2023 01:42:22 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 12 Apr 2023 01:42:23 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Apr 2023 01:42:24 GMT
USER ContainerAdministrator
# Wed, 12 Apr 2023 01:42:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Apr 2023 01:42:40 GMT
USER ContainerUser
# Wed, 12 Apr 2023 01:42:51 GMT
COPY dir:8214f6b15a617bff549fa1e8e973ad9cf58dcd41804c9c4d00b4aebf5303ecc4 in C:\openjdk-8 
# Wed, 12 Apr 2023 01:43:13 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:e06b772d586b58466a653b72002aee7c59496110e9ae402ff58f026e44452506`  
		Last Modified: Wed, 12 Apr 2023 02:34:14 GMT  
		Size: 122.3 MB (122328782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8058ec80ac2516d001291dea383d4abfa22416397a4c869e6fd79c0d4b64565f`  
		Last Modified: Wed, 12 Apr 2023 09:45:40 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ab65ec75a002055736a36c38ff72e20d2e2a38fbd592b8a39dc54d59c52ac2`  
		Last Modified: Wed, 12 Apr 2023 09:45:40 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945e56fe61cc0035312176b6a12cab89b60123d35096af6a223e34325ee0b14c`  
		Last Modified: Wed, 12 Apr 2023 09:45:40 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b218604ae9e3fa2e599373a83876742a01bf5607d06841bce5d44a23ad95960`  
		Last Modified: Wed, 12 Apr 2023 09:45:38 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5a2974beecc8e65d34f8ea71eaf46ba0cf50a7ba66d97e7bb76584ce87741c`  
		Last Modified: Wed, 12 Apr 2023 09:45:38 GMT  
		Size: 87.3 KB (87334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02493fa3c7ee2e1c38f49f9dad44450215bf93638dc65e07fb556918410ad978`  
		Last Modified: Wed, 12 Apr 2023 09:45:38 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ac4ec6a16142768abd7646ef92d4d498e487b760b05a31e413e6e80d276e84`  
		Last Modified: Wed, 12 Apr 2023 09:45:50 GMT  
		Size: 101.4 MB (101405216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37ac008407bb99d3b93415ea8acd97a8a63959a283e602cc45abdb494690a8c`  
		Last Modified: Wed, 12 Apr 2023 09:45:38 GMT  
		Size: 85.4 KB (85370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
