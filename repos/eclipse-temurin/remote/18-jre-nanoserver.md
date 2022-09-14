## `eclipse-temurin:18-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:d11ad0e0d21210c28f6026b099c1ea126626bd4ae9d9c6694c8cb33d6c16d387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:18-jre-nanoserver` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:d5e21e9d4bd84ffcd71a8985cc64bb9842cfb9d45ab6fb39632994f878cec57c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161419002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4849745e598ef5c6311ae53f5070ddd060f81790d4e9cc86910097f78cc1ec`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Sep 2022 20:11:22 GMT
RUN Apply image 10.0.20348.1006
# Wed, 14 Sep 2022 16:38:20 GMT
SHELL [cmd /s /c]
# Wed, 14 Sep 2022 16:42:23 GMT
ENV JAVA_VERSION=jdk-18.0.2.1+1
# Wed, 14 Sep 2022 16:42:24 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 14 Sep 2022 16:42:25 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 16:42:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Sep 2022 16:42:35 GMT
USER ContainerUser
# Wed, 14 Sep 2022 16:43:23 GMT
COPY dir:0f122a29933687aee1aeb1ed0bbcab77514458b9f4eb8e7fa2df7c081ea3d7bd in C:\openjdk-18 
# Wed, 14 Sep 2022 16:43:41 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:09629875cd6ee57fa551626fa2963d8b54718ba9acbf28e7cb5d684a9cb754d7`  
		Size: 118.1 MB (118131331 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:07f30e2ceaa03f6ac7b6e6f319083288f48d1fa2a61f36f51f516da241496976`  
		Last Modified: Wed, 14 Sep 2022 16:57:28 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a093f144715a97031aff6f46f023689d904c6bb88cc03212f4121cebf932ae6`  
		Last Modified: Wed, 14 Sep 2022 16:59:50 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1584bfd0ec971c8096527107b7a3477d5a61dc0f98f806b9ee8d5635cada90e8`  
		Last Modified: Wed, 14 Sep 2022 16:59:50 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105e258d722eb3cb0a0a73d4a5a674e2ee69a6809be6c0700d0ad6e56846e518`  
		Last Modified: Wed, 14 Sep 2022 16:59:50 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9e4dedce45e43eda32ee7f720b332286a80c80be4b55802ce868ced49165c7`  
		Last Modified: Wed, 14 Sep 2022 16:59:47 GMT  
		Size: 81.2 KB (81220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7dbb1c0198a081292588e3cfdeb70f811ab93ae31fc66320942c78d551d0b5`  
		Last Modified: Wed, 14 Sep 2022 16:59:47 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85e1687effbd6196bcfd222abc13629ac5c1d8540a1394f9544b1aad484999c`  
		Last Modified: Wed, 14 Sep 2022 17:00:32 GMT  
		Size: 43.1 MB (43138638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993485662f49916963ad418bb6a868e2d1d04839e0b2c6594c913520de8e15ab`  
		Last Modified: Wed, 14 Sep 2022 17:00:24 GMT  
		Size: 62.1 KB (62148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jre-nanoserver` - windows version 10.0.17763.3406; amd64

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
