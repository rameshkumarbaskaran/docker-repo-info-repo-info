## `openjdk:19-ea-1-nanoserver`

```console
$ docker pull openjdk@sha256:5acff095a0e1e200a86a715cb12c7755552005d7d043b7afec10c7d14d617867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `openjdk:19-ea-1-nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull openjdk@sha256:1a49938154d42ba8d2fd5f9c3c782a8b851ffe38b569f6ce8ac5976f70c5cfc0
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291143218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27747c07021f463a44eadba64c6d9b7ef74ff5bccadccb78d1b0d78158a898a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:13:20 GMT
SHELL [cmd /s /c]
# Tue, 14 Dec 2021 01:25:34 GMT
ENV JAVA_HOME=C:\openjdk-19
# Tue, 14 Dec 2021 01:25:35 GMT
USER ContainerAdministrator
# Tue, 14 Dec 2021 01:25:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 14 Dec 2021 01:25:49 GMT
USER ContainerUser
# Tue, 14 Dec 2021 01:25:50 GMT
ENV JAVA_VERSION=19-ea+1
# Tue, 14 Dec 2021 01:26:07 GMT
COPY dir:7010eebb09f7c20e73372f6d5b5462503856d1ac2288bd09ffd8a0a31357e9f8 in C:\openjdk-19 
# Tue, 14 Dec 2021 01:26:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 14 Dec 2021 01:26:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e60ec86b90e1492e0e0ed2cbebcf624990a34862e24207343fd85b84b3544c8e`  
		Last Modified: Wed, 10 Nov 2021 18:01:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be84735b5610fda61090aab5eb00c3a1116a66c95ead61b97f30d1dc374e4261`  
		Last Modified: Tue, 14 Dec 2021 01:34:42 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56dde0c29ae6ac9a3183d4667bd5625e7314d36dc46a23cf7eb6760471097156`  
		Last Modified: Tue, 14 Dec 2021 01:34:42 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e684f7e01b01f87e65f5437662e7274e066f2b599283a25f4bf31563711378`  
		Last Modified: Tue, 14 Dec 2021 01:34:43 GMT  
		Size: 70.8 KB (70758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6738809da261f07829ac38d0e4b6da6c7c1db60f90a73b286ca63ec1c5a36d8`  
		Last Modified: Tue, 14 Dec 2021 01:34:39 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2672c924624b201a2333c83991d3c90aecb076f7eb629355f96c17b3639021`  
		Last Modified: Tue, 14 Dec 2021 01:34:40 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d823d4d1d730d1f77a03909afa36d6dd78d2253f675cc110054011d06fd63a11`  
		Last Modified: Tue, 14 Dec 2021 01:38:04 GMT  
		Size: 184.8 MB (184768120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929c633df07364c600bbf720c6e6e9ed81bc854fa137059b907cba1a393dbb09`  
		Last Modified: Tue, 14 Dec 2021 01:34:40 GMT  
		Size: 3.5 MB (3514425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff10994d31dff7f5514113b522fe3d9b0e76626388ba207b1ae3e5f0e3cb18c7`  
		Last Modified: Tue, 14 Dec 2021 01:34:40 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
