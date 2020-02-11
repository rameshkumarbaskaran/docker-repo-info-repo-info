## `openjdk:15-ea-9-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:e2d4c80b742bc9297958a8fbe742a5090bc3645e98a9c2048518aa01c4ae73cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `openjdk:15-ea-9-jdk-nanoserver-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull openjdk@sha256:bd446e154c3a2447d58723b9d06bf6f33c5be023f77dc95dfe324467a1dc9048
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298463754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71598affa1f2b2179f3bc0a6aec5a553be114cb2a3204991e9954b68b51ce49`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Tue, 14 Jan 2020 23:56:11 GMT
SHELL [cmd /s /c]
# Tue, 14 Jan 2020 23:56:12 GMT
ENV JAVA_HOME=C:\openjdk-15
# Tue, 14 Jan 2020 23:56:13 GMT
USER ContainerAdministrator
# Tue, 14 Jan 2020 23:56:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Tue, 14 Jan 2020 23:56:31 GMT
USER ContainerUser
# Tue, 11 Feb 2020 01:30:03 GMT
ENV JAVA_VERSION=15-ea+9
# Tue, 11 Feb 2020 01:31:11 GMT
COPY dir:87e3b2676a806229f418f8d3c5ab950840e4bde9c98f5e3b949f384c6861006c in C:\openjdk-15 
# Tue, 11 Feb 2020 01:31:40 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Tue, 11 Feb 2020 01:31:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:764e25aa4e95684bd69a4d130dc1c729bfaef95293d9c76c4d2a12ced9e3a9ac`  
		Last Modified: Wed, 15 Jan 2020 01:51:06 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f193e511d66e393e8623d9efd86f48f82cc15ceb19ee3a6ac9da7343da044ad`  
		Last Modified: Wed, 15 Jan 2020 01:51:04 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fab357b0406f3be040eca20b497e3bdd7e731b95865fbfbe83acf826248583`  
		Last Modified: Wed, 15 Jan 2020 01:51:03 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fed5c1fef1ff77da19cbdb310981f89c791b7c4206a8b99d9a1f114b6a5a107`  
		Last Modified: Wed, 15 Jan 2020 01:51:03 GMT  
		Size: 70.0 KB (69974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dae8d73c31bd6bb443dd054e2ff7514c3f89f2252ad8f45b02d272a63de3194`  
		Last Modified: Wed, 15 Jan 2020 01:51:01 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f3c9d1711f4ec046e05ef23442610fe89e2d8b9abce561871695c5973b451`  
		Last Modified: Tue, 11 Feb 2020 01:46:12 GMT  
		Size: 925.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1eb7674eb34e71c3565e7271ffe470769b0a4b0e4f207a0f7ad7133c207a82`  
		Last Modified: Tue, 11 Feb 2020 01:46:33 GMT  
		Size: 193.9 MB (193893493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffad51b2153b043e169a7741a704dc3154dc821c230eef4c334a7ecb69efb69`  
		Last Modified: Tue, 11 Feb 2020 01:46:13 GMT  
		Size: 3.4 MB (3440426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f4bc44da27e6ada8cc91eb6ff38bfa4de3d07a80d67546fd6acf484b92d478`  
		Last Modified: Tue, 11 Feb 2020 01:46:12 GMT  
		Size: 919.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
