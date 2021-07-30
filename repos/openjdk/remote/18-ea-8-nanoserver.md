## `openjdk:18-ea-8-nanoserver`

```console
$ docker pull openjdk@sha256:af6f822575693c35b685684fffa6d8d0afcaf7555c699cbfc19f6ccca8a7c6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `openjdk:18-ea-8-nanoserver` - windows version 10.0.17763.2061; amd64

```console
$ docker pull openjdk@sha256:9795cbf794e470fffaee6ef5cf1ef7ea1bac8ba41ce9951c353702c3a398eb84
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289104790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32700b31af4d1772ccabcf3b684be69ef07663f72cda31d1eeb1a3c169d41afe`
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
# Fri, 30 Jul 2021 19:18:33 GMT
ENV JAVA_VERSION=18-ea+8
# Fri, 30 Jul 2021 19:18:51 GMT
COPY dir:bb264c58b2998d90282979d9952b64012dba209a04a77b67be912fe2dffffbdd in C:\openjdk-18 
# Fri, 30 Jul 2021 19:19:21 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 30 Jul 2021 19:19:24 GMT
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
	-	`sha256:3e5c81b0a088d5d6c87628149d7a9e6db21a4be2edf142be1f4874c9ca29ff08`  
		Last Modified: Fri, 30 Jul 2021 19:33:33 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d64138676eb6baf0cc79ab342af4ad1c1872c17e3bd5fc68db77ffce0578d58`  
		Last Modified: Fri, 30 Jul 2021 19:33:53 GMT  
		Size: 182.7 MB (182681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267bf23fa700f2f7e57a23301cede57f72c83fbfae90af3de079b33f95a3b303`  
		Last Modified: Fri, 30 Jul 2021 19:33:34 GMT  
		Size: 3.6 MB (3621199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1126b0e44aaae34b4c661302159eb120dae94ebbd9e74f7b73699a40ecda8207`  
		Last Modified: Fri, 30 Jul 2021 19:33:33 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
