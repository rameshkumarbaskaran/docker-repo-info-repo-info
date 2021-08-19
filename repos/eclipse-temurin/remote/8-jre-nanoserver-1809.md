## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:4cb1701f115c119ddcfaa13cfbca5e1d555b710a7c41c66c60cefc932de6cef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull eclipse-temurin@sha256:eea4c687c4bdc156920ed973f29456bb14cbf36fe1c27519fd38ec29cfeeb0a3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.0 MB (203033710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84dce4fbc858f82a4dbe9a3cee5d4dc2d61b08ac4909729dd2569cfad4eb8c97`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Aug 2021 19:15:20 GMT
RUN Apply image 1809-amd64
# Wed, 11 Aug 2021 17:30:38 GMT
SHELL [cmd /s /c]
# Fri, 13 Aug 2021 21:40:02 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Fri, 13 Aug 2021 21:40:04 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 13 Aug 2021 21:40:06 GMT
USER ContainerAdministrator
# Fri, 13 Aug 2021 21:40:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%         && setx /M PATH %JAVA_HOME%\bin;%PATH%         && echo Complete.
# Fri, 13 Aug 2021 21:40:30 GMT
USER ContainerUser
# Fri, 13 Aug 2021 21:40:43 GMT
COPY dir:6622177b1379d4d7267ebc9bc4d0bb013ea883bae36028c72b4045f7fa088598 in C:\openjdk-8 
# Thu, 19 Aug 2021 20:22:41 GMT
RUN echo Verifying install ...     && echo   java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:bc8517709e9cfff223cb034ff5be8fcbfa5409de286cdac9ae1b8878ebea6b84`  
		Size: 102.7 MB (102741177 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae0a5a946be2ad0e39a8260e454c0060a31a9f7e5be75d1f9038dc13730abc0a`  
		Last Modified: Wed, 11 Aug 2021 18:21:28 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39ae0f8395ca5409c69101b5dddc5639f72f78bc686a5768594bc7be468bf3b`  
		Last Modified: Fri, 13 Aug 2021 22:01:13 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f314f5e253839b8b66cceaa780f0e98c4fb9a831a491340e45bcabda54061e2e`  
		Last Modified: Fri, 13 Aug 2021 22:01:11 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd6b7337451ff1f56017b29155ddaaa31cede2680438e44411adcacc4332cdd`  
		Last Modified: Fri, 13 Aug 2021 22:01:09 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422054804bf6b6f8f889df650e876e05c0a9058abddbdf04d56e8f0330f8d913`  
		Last Modified: Fri, 13 Aug 2021 22:01:08 GMT  
		Size: 71.6 KB (71567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ecb38f97959bb2408a3ec34132826fe34d28d87a65b3771a7e091dc9037cda`  
		Last Modified: Fri, 13 Aug 2021 22:01:08 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4a5e3a811b8fa1f67da9296dad08d0868e6c3c2c7b0f69437eb4aa28dc50b8`  
		Last Modified: Fri, 13 Aug 2021 22:03:04 GMT  
		Size: 100.2 MB (100165249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7a2d9b7c80dace7b93f6b22d9d65441b18f231d698341671ece74ca68be8045`  
		Last Modified: Thu, 19 Aug 2021 20:26:18 GMT  
		Size: 49.8 KB (49847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
