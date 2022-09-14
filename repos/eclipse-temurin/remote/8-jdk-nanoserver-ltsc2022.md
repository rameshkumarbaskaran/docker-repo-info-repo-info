## `eclipse-temurin:8-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:426bd323d1b71b693484f6995f67e7e2a5439241ca79e9c205d0b6a06343efc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:b568f82f81d91991a31430ef408475e93b7ac18d7e402bde8855c014533f2a48
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218758228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5971e02317165e2357b29fc38786fc28298bcd28190232df35a8b78c77828078`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Sep 2022 20:11:22 GMT
RUN Apply image 10.0.20348.1006
# Wed, 14 Sep 2022 16:38:20 GMT
SHELL [cmd /s /c]
# Wed, 14 Sep 2022 16:38:21 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Wed, 14 Sep 2022 16:38:21 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 Sep 2022 16:38:22 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 16:38:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Sep 2022 16:38:37 GMT
USER ContainerUser
# Wed, 14 Sep 2022 16:38:48 GMT
COPY dir:3f2d3aa63ba7a56176deaae1ba1b26dbdbe105074828954c77b0da527aacd6d7 in C:\openjdk-8 
# Wed, 14 Sep 2022 16:39:03 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:09629875cd6ee57fa551626fa2963d8b54718ba9acbf28e7cb5d684a9cb754d7`  
		Size: 118.1 MB (118131331 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:07f30e2ceaa03f6ac7b6e6f319083288f48d1fa2a61f36f51f516da241496976`  
		Last Modified: Wed, 14 Sep 2022 16:57:28 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16323d7400627da10ce240f6e16c64f6ede4747acabd111c1f97f3ad620293ec`  
		Last Modified: Wed, 14 Sep 2022 16:57:29 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002ad03790aa608a5e569e2bb5524ab646f494ff6129d26716ae8b523a371076`  
		Last Modified: Wed, 14 Sep 2022 16:57:28 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15108493c7dc7578b06d64ea9a5472d2f923e209c7e0342954ba5f5de11379d`  
		Last Modified: Wed, 14 Sep 2022 16:57:26 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4b7ee065d4dfbef0b4508eb703bf0abaddfa3a39bdce741b72f9c1c1fa1e1c`  
		Last Modified: Wed, 14 Sep 2022 16:57:26 GMT  
		Size: 79.6 KB (79618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266593abc7831b07aa3367c5799233affe80baa3691fb02ec3f9207a5403d4d1`  
		Last Modified: Wed, 14 Sep 2022 16:57:26 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4a834df7059a1e2e704b02ea037d3a52f17963bcfd3314ae1933d426985f78`  
		Last Modified: Wed, 14 Sep 2022 16:57:38 GMT  
		Size: 100.5 MB (100480177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa21228b73836d634eeb540ae7f49a67603435e1280387e244ba1c0420068e23`  
		Last Modified: Wed, 14 Sep 2022 16:57:26 GMT  
		Size: 62.0 KB (61961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
