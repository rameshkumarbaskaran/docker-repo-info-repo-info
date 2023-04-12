## `eclipse-temurin:20-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:62827b3fdade4a9c4bedf90e12f76f127507ff206a76c115ca5de50f25ba02ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1668; amd64

### `eclipse-temurin:20-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1668; amd64

```console
$ docker pull eclipse-temurin@sha256:1a4a8cbca514cbc3abc6e04079ed7ae4a00897d0dd2970db4414f71b527363f2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.2 MB (168231461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f879b350999e08c89e09a95a5cb6c30c062161ee94ef873652c59c6d089ed004`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 12 Apr 2023 01:48:41 GMT
COPY dir:88253b833ff2634324ea23b2cdfd627ca2e30273c5f29426251a8626a4f6baa7 in C:\openjdk-20 
# Wed, 12 Apr 2023 01:48:56 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:19b49903e9ed6af12f9fb83ea522287b16b4c276e34fe96ea7f0e444a9d99083`  
		Last Modified: Wed, 12 Apr 2023 09:48:42 GMT  
		Size: 45.8 MB (45753455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94bb6add05314ed9a1537fa4f48735778aa36cf1b5f6b935a5a90703d57dc47`  
		Last Modified: Wed, 12 Apr 2023 09:48:32 GMT  
		Size: 57.3 KB (57269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
