## `eclipse-temurin:11-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:6996143502b204a33de0e278ce620654a073c7121e5556ef086f0eba10f77352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `eclipse-temurin:11-nanoserver` - windows version 10.0.20348.1129; amd64

```console
$ docker pull eclipse-temurin@sha256:96d7c487c32865014b55c971149d96f871c578d1d12320d11dec122d7cf0ed2e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314686294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd073c624f3b05030104f6687dbd8feeca826c40083929f4b6806d792299d0c`
-	Default Command: `["jshell"]`
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
# Fri, 04 Nov 2022 23:41:27 GMT
COPY dir:cba9eceeddb80383417f5e5518328c343fc4183981a343fca253ea7c2e4dfda5 in C:\openjdk-11 
# Fri, 04 Nov 2022 23:41:50 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 04 Nov 2022 23:41:51 GMT
CMD ["jshell"]
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
	-	`sha256:dd7abdd8d3abc9c3f790cafd318954ff2a1ea1e3fe688d5850b92040303c0080`  
		Last Modified: Sat, 05 Nov 2022 00:27:53 GMT  
		Size: 192.5 MB (192528340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3fa2ac5c580bb4ac0d1d44a58e078f56bfc13ee26cba2d486793ec475afdee`  
		Last Modified: Sat, 05 Nov 2022 00:27:32 GMT  
		Size: 60.8 KB (60768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7550e214eb41d9928f123e2a20ee5d667c7d097b6cd354f22e720b64a8653e`  
		Last Modified: Sat, 05 Nov 2022 00:27:32 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-nanoserver` - windows version 10.0.17763.3532; amd64

```console
$ docker pull eclipse-temurin@sha256:2b0793d7936c6a0af98d67f46a3fdab37419bebed4dc26c4b9d5742006b3d8bd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299462294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c046717498646ed731a99144711befff5ccf1b25b16d9eaece8004372c7b4a`
-	Default Command: `["jshell"]`
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
# Fri, 04 Nov 2022 23:32:19 GMT
COPY dir:cba9eceeddb80383417f5e5518328c343fc4183981a343fca253ea7c2e4dfda5 in C:\openjdk-11 
# Fri, 04 Nov 2022 23:32:41 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 04 Nov 2022 23:32:42 GMT
CMD ["jshell"]
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
	-	`sha256:e0910696d9f121a91814ed46e3ddca317d7a118f42f38f9a79644efbae11cbc1`  
		Last Modified: Sat, 05 Nov 2022 00:25:08 GMT  
		Size: 192.5 MB (192523586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528d324315c36124eca47d6e6458ae82ec4c86e520728e5547661b77b74466f8`  
		Last Modified: Sat, 05 Nov 2022 00:24:48 GMT  
		Size: 90.2 KB (90231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ae40eb53435fef4d6ed2467d40f8445ab80955e500ef602790c1db578a5d90`  
		Last Modified: Sat, 05 Nov 2022 00:24:48 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
