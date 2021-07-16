## `openjdk:18-ea-6-nanoserver`

```console
$ docker pull openjdk@sha256:698ce252f7f2be49009e4394a24f9b4208e6dbc6fcd1717750843fa60617bd99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `openjdk:18-ea-6-nanoserver` - windows version 10.0.17763.2061; amd64

```console
$ docker pull openjdk@sha256:5b48836aa4daadbf38bb8c0d6959d99fea9a24324fe4c7fd42b093c1431a7eab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289151154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b85c74ca601619896d39e5b284e2f779b0059d88f9c98c2a1521b2db9501bc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:53:30 GMT
SHELL [cmd /s /c]
# Wed, 14 Jul 2021 02:53:36 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 14 Jul 2021 02:53:44 GMT
USER ContainerAdministrator
# Wed, 14 Jul 2021 02:54:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Jul 2021 02:54:08 GMT
USER ContainerUser
# Thu, 15 Jul 2021 22:19:04 GMT
ENV JAVA_VERSION=18-ea+6
# Thu, 15 Jul 2021 22:19:24 GMT
COPY dir:e5081a177429aea0a3f81bd7ef48fec816a745bda2e5ed98a61522b3b0beb39e in C:\openjdk-18 
# Thu, 15 Jul 2021 22:19:52 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 15 Jul 2021 22:19:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d8754fb12dd351c91bed29d92c703cddb135a78d8f056b6a3bf13a251c1d2d`  
		Last Modified: Wed, 14 Jul 2021 03:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89509de1f10eea36c6e14a8f32bc735a7e52e07235bb588c9dff480855c851c0`  
		Last Modified: Wed, 14 Jul 2021 03:42:25 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a172401c9271ad5ee8356c8f36a409f68259854e9de596e04069a2a176db3c6`  
		Last Modified: Wed, 14 Jul 2021 03:42:25 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3247de649752bd08242527a227d09c6398c2676025c2527f3b65c5c8cd032886`  
		Last Modified: Wed, 14 Jul 2021 03:42:24 GMT  
		Size: 69.9 KB (69948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1baf3b57ea2d376291b5174f1db66c9b8d971170b6ec871bdbd1fc496e82d65`  
		Last Modified: Wed, 14 Jul 2021 03:42:22 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093161c33ab74abbb08080c086a2736686d64728074013f5a9f9b654c6b7b1a6`  
		Last Modified: Thu, 15 Jul 2021 22:33:57 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0569740fd61e9965c4c5fd292ad6f9b8d97d8f7210a365b6b9d0761734413747`  
		Last Modified: Thu, 15 Jul 2021 22:37:16 GMT  
		Size: 182.7 MB (182701901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a10cc0c5ea68b640c9d50f8761f48766da737280deca1b6aaaeae2656ab303`  
		Last Modified: Thu, 15 Jul 2021 22:33:58 GMT  
		Size: 3.6 MB (3646786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c306a532e4f9885df8de66584734b1f0ecd4a6e7b157bad5c690a5c2b92d435`  
		Last Modified: Thu, 15 Jul 2021 22:33:57 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
