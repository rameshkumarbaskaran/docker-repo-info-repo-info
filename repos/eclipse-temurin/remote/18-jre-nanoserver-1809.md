## `eclipse-temurin:18-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:bc34be2a8bd9ca141d023dfbd09c2ddb3ed41dd81e69b60b5e4962869a8ca2b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:18-jre-nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull eclipse-temurin@sha256:3349573b858599640266f7e7962269a146b3fc826f172a73df2fc3675a0a52ed
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.5 MB (149502903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4043e99e00162d2e9de20c3a84cc94755a5da8a864bb39928a12fa8863634feb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 16:03:00 GMT
SHELL [cmd /s /c]
# Wed, 14 Sep 2022 16:32:58 GMT
ENV JAVA_VERSION=jdk-18.0.2.1+1
# Wed, 14 Sep 2022 16:32:59 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 14 Sep 2022 16:33:00 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 16:33:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Sep 2022 16:33:09 GMT
USER ContainerUser
# Wed, 14 Sep 2022 16:37:55 GMT
COPY dir:0f122a29933687aee1aeb1ed0bbcab77514458b9f4eb8e7fa2df7c081ea3d7bd in C:\openjdk-18 
# Wed, 14 Sep 2022 16:38:11 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:233f09b2a52487084f2cfb5e06dac2815651432c9d37c729582f59cfcf66b243`  
		Last Modified: Wed, 14 Sep 2022 16:47:12 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a350d08f2ed032e24a5320519566197931177aa31b5e885df487768aa2d5f5`  
		Last Modified: Wed, 14 Sep 2022 16:55:55 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c756bccc16e99f889fd3cddef91c4c843400008c3236a93d522dd8bc69cce823`  
		Last Modified: Wed, 14 Sep 2022 16:55:55 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042bd3a9ce1e44b5ff9dcfe43afee3fad7b479a685801f33f3a34f6da4f5a995`  
		Last Modified: Wed, 14 Sep 2022 16:55:54 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3b136eeda7e8702846403916f3e784b1e6c907e6bc2f75959527c202b647ef`  
		Last Modified: Wed, 14 Sep 2022 16:55:52 GMT  
		Size: 68.4 KB (68403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03d8d62f82ad88c842779be7d22f04938ffd988a725584682799412da4f8d3b`  
		Last Modified: Wed, 14 Sep 2022 16:55:52 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d438a5b408403658c255667344f9d4875fe3111ad7ddefe8ca24829e4e21d8a8`  
		Last Modified: Wed, 14 Sep 2022 16:57:16 GMT  
		Size: 43.2 MB (43152722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24bbace5f9dcc7f11c9ff44af421f4520b032db5e938059b1e13787d99d1ba9`  
		Last Modified: Wed, 14 Sep 2022 16:57:07 GMT  
		Size: 2.9 MB (2941874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
