## `eclipse-temurin:20-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8ca2a44d6d59bfa9ab5dbfb9b7d6612ce5b0f627f5552fd6e66229827e723966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1668; amd64

### `eclipse-temurin:20-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.1668; amd64

```console
$ docker pull eclipse-temurin@sha256:a69c7e62cb3b6327eab70ff091596475b4fdd12e569f2ad760a16dc2f263f185
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.7 MB (317736810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c56bb0445eef2d4b58f353d1c9c0ffc7c1bc8b2aaba4afa76fffc52cd00719`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:16 GMT
RUN Apply image 10.0.20348.1668
# Wed, 12 Apr 2023 01:42:21 GMT
SHELL [cmd /s /c]
# Wed, 12 Apr 2023 01:47:28 GMT
ENV JAVA_VERSION=jdk-20+36
# Wed, 12 Apr 2023 01:47:29 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 12 Apr 2023 01:47:29 GMT
USER ContainerAdministrator
# Wed, 12 Apr 2023 01:47:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Apr 2023 01:47:40 GMT
USER ContainerUser
# Wed, 12 Apr 2023 01:47:56 GMT
COPY dir:0bba24b8a26333fabbf995368b29d05051d1ff1f33d04d60afd33310da1fd9b4 in C:\openjdk-20 
# Wed, 12 Apr 2023 01:48:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Apr 2023 01:48:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e06b772d586b58466a653b72002aee7c59496110e9ae402ff58f026e44452506`  
		Last Modified: Wed, 12 Apr 2023 02:34:14 GMT  
		Size: 122.3 MB (122328782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8058ec80ac2516d001291dea383d4abfa22416397a4c869e6fd79c0d4b64565f`  
		Last Modified: Wed, 12 Apr 2023 09:45:40 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d771ecdf092529e0c97bd1e4f0a478bf6923159b17d1650d091f062627e215c7`  
		Last Modified: Wed, 12 Apr 2023 09:47:58 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c60e8241e702088dc2ffcc30dc7902f7e53ae5f0e7b203b03811dff7ce9684`  
		Last Modified: Wed, 12 Apr 2023 09:47:57 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784c970ac0afccfe355779fa5ead00807dda21bf87b1faf2ff0fa8a9cfae3d76`  
		Last Modified: Wed, 12 Apr 2023 09:47:57 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5061be6624f789f71935eaf2a00de889b24c06e42f237d96b99e3cb720d2086`  
		Last Modified: Wed, 12 Apr 2023 09:47:56 GMT  
		Size: 86.6 KB (86612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0da7e587c56006cb75a21efef088296fcbb73f6c2a2cf780b8baf4f2144dfd`  
		Last Modified: Wed, 12 Apr 2023 09:47:55 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbab285f9a15b8338c2cbb45532b1836ccb5a66718f1796e6ed303b4f56457a`  
		Last Modified: Wed, 12 Apr 2023 09:48:20 GMT  
		Size: 195.2 MB (195241477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5ccfdcd850e7a0f71861f94d95933ac88ddb5656b64410f293efbaba20faff`  
		Last Modified: Wed, 12 Apr 2023 09:47:56 GMT  
		Size: 73.5 KB (73466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9a02e18ef9e60ac3cf787af4eb5a20e4ab9a77390a624c05a66ca3e20aee13`  
		Last Modified: Wed, 12 Apr 2023 09:47:55 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
