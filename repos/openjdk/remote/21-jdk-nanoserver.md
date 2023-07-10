## `openjdk:21-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:0327c963dd58c555f2b46b04956083da35c61b24ebd14c79b2a439dcdd8e0777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `openjdk:21-jdk-nanoserver` - windows version 10.0.17763.4499; amd64

```console
$ docker pull openjdk@sha256:46a287f42199f0216d86b27e51f8156bccf0a002cb59c9b4b49105b35f9e0730
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.3 MB (306260616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d278993dc50e2b6f9b89c8fdf41071dcccc4a8afc418b1309441a37827bc2b47`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 21 Jun 2023 07:40:33 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:41:51 GMT
SHELL [cmd /s /c]
# Sat, 24 Jun 2023 03:10:41 GMT
ENV JAVA_HOME=C:\openjdk-21
# Sat, 24 Jun 2023 03:10:42 GMT
USER ContainerAdministrator
# Sat, 24 Jun 2023 03:10:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 24 Jun 2023 03:10:52 GMT
USER ContainerUser
# Mon, 10 Jul 2023 19:25:46 GMT
ENV JAVA_VERSION=21-ea+30
# Mon, 10 Jul 2023 19:26:01 GMT
COPY dir:ba412bb2d7ad2b7e57d328f451e834336702f588090d7ff41597b585425c9b30 in C:\openjdk-21 
# Mon, 10 Jul 2023 19:26:15 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 10 Jul 2023 19:26:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:09087aac643f57e5e24f95fe0a1c8519d0f93dfcf4500263516c0f3874290109`  
		Last Modified: Fri, 23 Jun 2023 02:23:11 GMT  
		Size: 104.4 MB (104400893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09be2e47b3dff420361e93d34eaadedcfd9549c9be5bd77936370792babf874`  
		Last Modified: Sat, 24 Jun 2023 01:24:43 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1761082022ac41b0f9e56c60b660a94c5cc48216abc4ee6585d75e5f639b8b83`  
		Last Modified: Sat, 24 Jun 2023 03:15:39 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3d43ae3625180a30ce5075af37248f9b8bfb36b35d98ea87e0c69dd6309c66`  
		Last Modified: Sat, 24 Jun 2023 03:15:39 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7bf66e4a671426e237a857427cbba03c02b51ed5e66b0d72fc65d78ec04f91`  
		Last Modified: Sat, 24 Jun 2023 03:15:39 GMT  
		Size: 67.2 KB (67224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68960e43d220da8539c1fcad0e31945a1a70a4be19f3182a2d989413baa9e212`  
		Last Modified: Sat, 24 Jun 2023 03:15:37 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2ac3b1bc728848652b2cc6303db357589d50a0af1473bc950881eb7578e093`  
		Last Modified: Mon, 10 Jul 2023 20:20:16 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c13824b27ded4e3d5ae76cefd8061289c53192076b6da8bd648729a80c675a5`  
		Last Modified: Mon, 10 Jul 2023 20:20:36 GMT  
		Size: 198.0 MB (197982514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf99cb518e6a65da94da4e58cdd38678ac6c83513c76f75ec8b7b314eacca496`  
		Last Modified: Mon, 10 Jul 2023 20:20:17 GMT  
		Size: 3.8 MB (3803073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775f3c422b649e7b7f8e5c9bc39eb7b0b9dc5b5094894129311258537df5d614`  
		Last Modified: Mon, 10 Jul 2023 20:20:16 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
