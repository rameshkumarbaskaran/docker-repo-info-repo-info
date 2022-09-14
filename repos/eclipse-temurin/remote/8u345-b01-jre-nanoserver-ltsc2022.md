## `eclipse-temurin:8u345-b01-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:da77839619b03eadef0e6d8d3fbe9dad0bae9577da0c31b2d77f4945f2e608ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `eclipse-temurin:8u345-b01-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:ae1a738e9b1a4dad4f15bfba54b80ad89a95aa1052e413fb1ce46dbd029733a4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157596169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5563534805441b67d6b7cd639c2472864b3926ed99c9400a1402285d93b97ce`
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
# Wed, 14 Sep 2022 16:39:18 GMT
COPY dir:8b6137b055df5a3c6f914a172c41a8287046696fe7ccc91d96608246e3752adc in C:\openjdk-8 
# Wed, 14 Sep 2022 16:39:33 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:23518ba784d3409ab46e29ec691c9f89396c93193a2d859f418ecdd025bc066c`  
		Last Modified: Wed, 14 Sep 2022 16:57:57 GMT  
		Size: 39.3 MB (39318099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277caa8ca3f13bb69a0e5722b525af3489207134324e08609f6f2b29ccd2c226`  
		Last Modified: Wed, 14 Sep 2022 16:57:51 GMT  
		Size: 62.0 KB (61980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
