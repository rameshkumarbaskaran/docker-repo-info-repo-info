## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:65a248445970aa61e2c46e6e8b77c1a74cacc4913079a54fc6b3885f3140abd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1668; amd64
	-	windows version 10.0.17763.4252; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.1668; amd64

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

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.17763.4252; amd64

```console
$ docker pull eclipse-temurin@sha256:aca26b491d93e68003953bd976d6ea10369ef94ebfe40b85905ec73fe8923aa5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (296008695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442c200f322b7883cf286e9dd91c9f85a525d358ea267796d9dd38de02fe8ef8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Tue, 11 Apr 2023 23:45:41 GMT
SHELL [cmd /s /c]
# Wed, 12 Apr 2023 01:25:11 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Wed, 12 Apr 2023 01:25:12 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Apr 2023 01:25:13 GMT
USER ContainerAdministrator
# Wed, 12 Apr 2023 01:25:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Apr 2023 01:25:24 GMT
USER ContainerUser
# Wed, 12 Apr 2023 01:25:39 GMT
COPY dir:b9d1887161cde3cc24ae2101d8a284bfc20814b15fed427bc1c905c1248fb0bf in C:\openjdk-17 
# Wed, 12 Apr 2023 01:25:59 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Apr 2023 01:26:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af799fb2ff133c89311c6a42d34b8cb6c9b11d775f52e04ab08389d05e64ed1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:10 GMT  
		Size: 106.8 MB (106788951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1db438f20b81fe0c031e4e3eee58d278fba7258d01057ff18964cccf70d41c`  
		Last Modified: Wed, 12 Apr 2023 00:52:38 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d940edd2c169dbe97e28eaac688f773a26971f49cbce0c580dec219c0a091a6`  
		Last Modified: Wed, 12 Apr 2023 09:40:59 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68cf891bc434751fa3e0d43803d1d1b3966b15191058fd5bf2d9f3f70340008`  
		Last Modified: Wed, 12 Apr 2023 09:40:59 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1662ed07c1d02bbfbbd979a470af707c2e65c7d8de779c6e791ca43a34f7ec`  
		Last Modified: Wed, 12 Apr 2023 09:40:59 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2804a413fa32f1ac8096607d75ad6a983b2755f9d7994a3275faa45ad68b44`  
		Last Modified: Wed, 12 Apr 2023 09:40:57 GMT  
		Size: 71.3 KB (71299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddad53a51d13c426f8e7d899d76b648e9ca0201514f6c69c5335ffc180da6eb0`  
		Last Modified: Wed, 12 Apr 2023 09:40:56 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b25cf6e88454497cad74f97cd7b257e75b668c766d93adb969ea922db64f874`  
		Last Modified: Wed, 12 Apr 2023 09:41:18 GMT  
		Size: 185.5 MB (185476505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7939fd9463285685a5ae3cbbc0542c20afb3684f0541f7e28f9c67033f06d1e`  
		Last Modified: Wed, 12 Apr 2023 09:40:58 GMT  
		Size: 3.7 MB (3665042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e92f69836767d591945350f6170936fa85287b8dfc2f3143605d9f2a0e3c4fc`  
		Last Modified: Wed, 12 Apr 2023 09:40:56 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
