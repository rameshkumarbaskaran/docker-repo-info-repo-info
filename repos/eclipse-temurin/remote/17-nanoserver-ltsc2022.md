## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:890e69f7042cd98cd62c8634497963c16983b83ec87455960623e75e7cf692b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1668; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.1668; amd64

```console
$ docker pull eclipse-temurin@sha256:500a14078eb46a34a20b730183cc9fc6d5b760ab7764af8a8f658e7333d431ff
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.0 MB (307965330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e410305744cbbabd581da24aa41492a8342865310574100a28d77ae416ce6f76`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:16 GMT
RUN Apply image 10.0.20348.1668
# Wed, 12 Apr 2023 01:42:21 GMT
SHELL [cmd /s /c]
# Wed, 12 Apr 2023 01:45:50 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Wed, 12 Apr 2023 01:45:51 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Apr 2023 01:45:51 GMT
USER ContainerAdministrator
# Wed, 12 Apr 2023 01:46:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Apr 2023 01:46:03 GMT
USER ContainerUser
# Wed, 12 Apr 2023 01:46:19 GMT
COPY dir:b9d1887161cde3cc24ae2101d8a284bfc20814b15fed427bc1c905c1248fb0bf in C:\openjdk-17 
# Wed, 12 Apr 2023 01:46:42 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Apr 2023 01:46:42 GMT
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
	-	`sha256:bbccf86aba754c96fec3392364249e60424924cb4ecd3ef3fd1173fdf59dbd0a`  
		Last Modified: Wed, 12 Apr 2023 09:47:08 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a6af2e3b4b49b11dafa6baa7abb7124b85b7dffaada1e60410f3b182b5440d`  
		Last Modified: Wed, 12 Apr 2023 09:47:08 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23fbea9a6aad406b2f0d73eebd255c578b52cb3d992e90d1a490dcef510c127`  
		Last Modified: Wed, 12 Apr 2023 09:47:08 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0853e1de5f76cccd350c367db8bff4fcad9ca15d2bd1905bfdf6d9ff5bc745`  
		Last Modified: Wed, 12 Apr 2023 09:47:06 GMT  
		Size: 81.3 KB (81333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c1ec806b6b017a38be0ba594da25d03f5079eb81ca9e62a9dd176c6c78465b`  
		Last Modified: Wed, 12 Apr 2023 09:47:06 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc645a1dd7342d4fc665c118533cfb75a0a30ccae1ef318b7d6db9eba8433ee`  
		Last Modified: Wed, 12 Apr 2023 09:47:27 GMT  
		Size: 185.5 MB (185457422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fad63c70427b8d5fb7d09c84cbf36510c9e184a9b3b17eca7eaf6a9c2b629c`  
		Last Modified: Wed, 12 Apr 2023 09:47:06 GMT  
		Size: 91.4 KB (91416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe58211ccf72b7615468ac8b1f93fad11b7bfd10d8b27708c283a1079d3bb89`  
		Last Modified: Wed, 12 Apr 2023 09:47:06 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
