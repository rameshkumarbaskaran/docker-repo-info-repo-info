## `openjdk:8-nanoserver`

```console
$ docker pull openjdk@sha256:403d0dbd0d34916401edc7cffe7de1e71acdc4061955f68a28766ad03a13d96c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `openjdk:8-nanoserver` - windows version 10.0.17763.2452; amd64

```console
$ docker pull openjdk@sha256:88b7db4e47628bf8fefa5477ea74bf6db8bdd138fb1f09a9d21ff2a1898db0ca
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.3 MB (204281811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0517159260c69b9985acc63a0043798d2cd8a74eb3c8d45d1c357bd065605aa`
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
# Wed, 12 Jan 2022 05:59:31 GMT
COPY dir:3a5581b2700e30ac96b7aaa667bdc25cdca1d6451f9f3d58913682ddf8d74e71 in C:\openjdk-8 
# Wed, 12 Jan 2022 05:59:44 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version 	&& echo Complete.
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
	-	`sha256:d8a7866b4f451abe494a60193dbd140f9d850bb80ae37dd1c972191e4bde0bd0`  
		Last Modified: Wed, 12 Jan 2022 23:20:55 GMT  
		Size: 101.1 MB (101072811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f08c08d3ba14007ede5e86cf1f6e3508d8b31dc716dabd243e3d3b32d2bb2`  
		Last Modified: Wed, 12 Jan 2022 23:20:42 GMT  
		Size: 103.0 KB (103036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
