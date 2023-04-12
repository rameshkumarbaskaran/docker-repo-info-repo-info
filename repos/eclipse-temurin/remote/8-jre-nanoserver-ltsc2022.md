## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:274c8915864c0a6ecf4550eaec95643d4222f66bc73949219ebcfe08099b0002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1668; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1668; amd64

```console
$ docker pull eclipse-temurin@sha256:4c4d3987afd72006b59414af7d7e38a6199437e5e873dc25c6fc4b2a6e277b62
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162409285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c6b0331f36eb3cb12c577715a34da60c5e88b0fbb9503cc8d118e7875fecce`
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
# Wed, 12 Apr 2023 01:43:31 GMT
COPY dir:dcd2674e91fb412db18990a7004f7a484148b702bd6de08f5ae3a3d6f6a3f6f8 in C:\openjdk-8 
# Wed, 12 Apr 2023 01:43:49 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:8f0713deb050e4abf548657de86df9a1f3e37f5cea770877cb6ad531ce83aad6`  
		Last Modified: Wed, 12 Apr 2023 09:46:09 GMT  
		Size: 39.9 MB (39929240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386067c122827f02f6c54b5f424f826adb07cbb6a3cf2136f4605812f1e4a5e2`  
		Last Modified: Wed, 12 Apr 2023 09:46:02 GMT  
		Size: 58.5 KB (58550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
