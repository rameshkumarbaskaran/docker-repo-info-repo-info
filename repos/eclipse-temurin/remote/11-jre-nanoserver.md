## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:967600c01cd47af1b3c150f6f4b7dfdd396aa1f48b30ad497311f8cfb8c2025b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.1129; amd64

```console
$ docker pull eclipse-temurin@sha256:bb091f5e11085ccffc6eb57183504ead1cdea6210072d80c16643dfd7ee75cc6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.1 MB (165116613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c990505fd3f7d80e7732cb983fee0bea0402b0da2085100cdaa943a4de4198`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Oct 2022 21:37:41 GMT
RUN Apply image 10.0.20348.1129
# Wed, 12 Oct 2022 15:54:21 GMT
SHELL [cmd /s /c]
# Fri, 04 Nov 2022 23:40:57 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:40:57 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 04 Nov 2022 23:40:59 GMT
USER ContainerAdministrator
# Fri, 04 Nov 2022 23:41:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 04 Nov 2022 23:41:11 GMT
USER ContainerUser
# Fri, 04 Nov 2022 23:42:07 GMT
COPY dir:f12bd30467bc1b7f61ca05a6124e6eb838888f3685c56f372d6fed2165b193b1 in C:\openjdk-11 
# Fri, 04 Nov 2022 23:42:24 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:b6520318982addabaf67d0cef5499282d15348f205cf5d7328925bcd681e85bd`  
		Last Modified: Tue, 25 Oct 2022 22:04:15 GMT  
		Size: 122.0 MB (122003513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ed0041e3584df1952980c3f73fd2b6e154328c7a0165f37dbe92ef94ae8a95`  
		Last Modified: Wed, 12 Oct 2022 16:12:53 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50e97dd6eef478e139210cbbc88b8a03dd9d8c463e1c87a9dea234a44750bbd`  
		Last Modified: Sat, 05 Nov 2022 00:27:35 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4cdcfda9423bb16a706acc0eef32a8554202a9adf426850e0ed48fd96e8a04`  
		Last Modified: Sat, 05 Nov 2022 00:27:35 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5e1e767a85bbcba7ca5e16371f1c7a1c6e4589ea4344fd407edbfb3d8bccfe`  
		Last Modified: Sat, 05 Nov 2022 00:27:34 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f3613fdbe1fb64c8fb1e23a2a42536ee39a5ac8b19d030f1744d43c910e37b`  
		Last Modified: Sat, 05 Nov 2022 00:27:32 GMT  
		Size: 86.8 KB (86754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb67a78665e5ccc0feb0a83bc602716ed16d4ddccfb5e25d9e77e5c9bc541f54`  
		Last Modified: Sat, 05 Nov 2022 00:27:32 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc3b642bfa1f262f63eba2b8813cf3519719e581024c6005dea9b58eb3aeb72`  
		Last Modified: Sat, 05 Nov 2022 00:28:15 GMT  
		Size: 43.0 MB (42959833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a772586845d1e347cd608144ee7ec7a488311cf919e47dd4a4c3929ec999c4f6`  
		Last Modified: Sat, 05 Nov 2022 00:28:06 GMT  
		Size: 60.8 KB (60785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.3532; amd64

```console
$ docker pull eclipse-temurin@sha256:6f3a8b1a28a92bf2920eafa40ae17d52c359bba442932fe2401456983100b36d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149893374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07bb7ae005340363f90a69043e41825a9fea63d934f24844b3f6baefe0be313`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Wed, 12 Oct 2022 15:20:49 GMT
SHELL [cmd /s /c]
# Fri, 04 Nov 2022 23:31:52 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:31:53 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 04 Nov 2022 23:31:54 GMT
USER ContainerAdministrator
# Fri, 04 Nov 2022 23:32:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 04 Nov 2022 23:32:04 GMT
USER ContainerUser
# Fri, 04 Nov 2022 23:37:24 GMT
COPY dir:f12bd30467bc1b7f61ca05a6124e6eb838888f3685c56f372d6fed2165b193b1 in C:\openjdk-11 
# Fri, 04 Nov 2022 23:37:55 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:ce29f4214f0fb0200b149c387d5e94ee47d5705e9bc7b884331390782282065f`  
		Last Modified: Thu, 27 Oct 2022 21:23:38 GMT  
		Size: 106.8 MB (106773776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6a667d76c19fca171390d60fb90c40e16c777050e943a7fe17ad7686841f0f`  
		Last Modified: Wed, 12 Oct 2022 16:02:59 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6d0b6a807744a73602c0bba2fbbbcd382a11c2afc29ca523a05dc2c1e4641`  
		Last Modified: Sat, 05 Nov 2022 00:24:51 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf22b895f3b27af90f8e0ed0c4d1ff3cffbf06f0ba534b9bd2dd337d0b4abc9c`  
		Last Modified: Sat, 05 Nov 2022 00:24:51 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8dbc771c48ed83d7556af788b27f5afb20020f8f3dc85cf700366631b2b638`  
		Last Modified: Sat, 05 Nov 2022 00:24:51 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e573968d0437720969bf4e82149cca5c58caa14a494df6be180389c1b897fa5`  
		Last Modified: Sat, 05 Nov 2022 00:24:48 GMT  
		Size: 67.8 KB (67813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1389b3fa34a674c4654b99ea5befddda5b09b29714a5d2afd3d9c93e6e46a55`  
		Last Modified: Sat, 05 Nov 2022 00:24:48 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06db7b2003ab5103344365e5cabf0dcb91e7aae912ec0c8b05577e5cb502b15f`  
		Last Modified: Sat, 05 Nov 2022 00:26:26 GMT  
		Size: 43.0 MB (42954497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40cca3c575b2ff90f5146d23451a6a44426cea76e2bdaf05ad7f92980354823`  
		Last Modified: Sat, 05 Nov 2022 00:26:15 GMT  
		Size: 91.6 KB (91561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
