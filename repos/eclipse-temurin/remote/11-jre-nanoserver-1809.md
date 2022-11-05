## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:af8d62bdbf7a7c1d2f1de48127073b078d3d2801e35f13ee0b2580b98b5eb207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.3532; amd64

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
