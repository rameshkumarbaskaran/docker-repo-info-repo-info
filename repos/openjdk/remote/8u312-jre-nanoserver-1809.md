## `openjdk:8u312-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:135518748e783164df9f9154661eb3b387a0219fdf581d69b4d52318cc11ccd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `openjdk:8u312-jre-nanoserver-1809` - windows version 10.0.17763.2452; amd64

```console
$ docker pull openjdk@sha256:2f12982fc4aa477c6e04f87c713cd64cde248d12f35898156aeb69ca8625f213
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141433608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954d2c3b3830ca71875da9ed2774afbc73a11392fa69d31a73319462e41e376e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 05:19:56 GMT
SHELL [cmd /s /c]
# Wed, 12 Jan 2022 05:58:57 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Jan 2022 05:58:58 GMT
USER ContainerAdministrator
# Wed, 12 Jan 2022 05:59:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 Jan 2022 05:59:08 GMT
USER ContainerUser
# Wed, 12 Jan 2022 05:59:09 GMT
ENV JAVA_VERSION=8u312
# Wed, 12 Jan 2022 06:03:41 GMT
COPY dir:d01eca1f47b40119ea7401e87f8309ebbb3c59555f496ebfb4562b12d58cd948 in C:\openjdk-8 
# Wed, 12 Jan 2022 06:03:55 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:71dcb756adb8534a87210067788d6aa4a5a366b72d022b7af035e5263a3e54a0`  
		Last Modified: Wed, 12 Jan 2022 16:05:17 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d242ab6d365769bbb33ecefd9af8e7517920572c91a5b34d10c022b83e6191c`  
		Last Modified: Wed, 12 Jan 2022 23:20:44 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6dbaa635bfc879256459b6e0b8ed22a7eda19fa621d12ec0910d382ba4c39f`  
		Last Modified: Wed, 12 Jan 2022 23:20:44 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61003df219647d8dc8102281772888d92b0ecc83ca2557ece3600dec8733734`  
		Last Modified: Wed, 12 Jan 2022 23:20:42 GMT  
		Size: 69.1 KB (69124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d467d53358fc22cb37dde7ae6d9ed816c8f5d70097f9c4e70727fa8292a536`  
		Last Modified: Wed, 12 Jan 2022 23:20:41 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a673f8a2d18cdba53f7daeb9ad3cb1046ea191b72986ed511007478fdd28c3c`  
		Last Modified: Wed, 12 Jan 2022 23:20:41 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaccb9970a3d9cb230891c7b0c33dee017f6c1a4c239408bb014bb4af278f429`  
		Last Modified: Wed, 12 Jan 2022 23:22:41 GMT  
		Size: 38.2 MB (38230105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f563e8de675ccb964911737a3005f7c1c045b6b5616b3f10edccaf9c0eec18`  
		Last Modified: Wed, 12 Jan 2022 23:21:59 GMT  
		Size: 97.5 KB (97539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
