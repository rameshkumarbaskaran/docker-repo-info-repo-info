## `eclipse-temurin:11-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:4e4d4e52ae140914b170f095809be243c7dde13efb2d775dd40cc31d75bcb452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `eclipse-temurin:11-nanoserver-1809` - windows version 10.0.17763.3532; amd64

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
