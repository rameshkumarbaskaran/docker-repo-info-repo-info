## `openjdk:16-nanoserver-1809`

```console
$ docker pull openjdk@sha256:916c473f3afc53ab931d0bd366fb2dd9b8c123dd81cb579d6d19b7cd4e438271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `openjdk:16-nanoserver-1809` - windows version 10.0.17763.1757; amd64

```console
$ docker pull openjdk@sha256:a30f4206e29709fd60fe025619d47cd6b4190545ee882073c253b5bcd3609c60
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285181992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e360252c3ba54b5e9ee1ee649053ab83fa142f2712c7ec06015a46d74ac94a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Feb 2021 13:06:30 GMT
RUN Apply image 1809-amd64
# Wed, 10 Feb 2021 16:45:48 GMT
SHELL [cmd /s /c]
# Wed, 10 Feb 2021 16:51:35 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 10 Feb 2021 16:51:35 GMT
USER ContainerAdministrator
# Wed, 10 Feb 2021 16:51:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Feb 2021 16:51:45 GMT
USER ContainerUser
# Wed, 10 Feb 2021 16:51:46 GMT
ENV JAVA_VERSION=16
# Wed, 10 Feb 2021 16:51:58 GMT
COPY dir:8cfdd9250e382800ba1fb4a6be20f45b5dda5b9351262a1210a73a6ffb109ce7 in C:\openjdk-16 
# Wed, 10 Feb 2021 16:52:12 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 10 Feb 2021 16:52:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ba17af31b9276ee11fdf859681b442db50979a39eff4cea2a559a5755cedbe01`  
		Size: 101.4 MB (101406193 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:89effbaeeb74323a670701c3b9dac248927e603ffb2d7efed14d993d32f7c183`  
		Last Modified: Wed, 10 Feb 2021 17:17:35 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e2b6006f062c42eea443494c05d8c64e4164602bfc37d6771cb61c259a328e`  
		Last Modified: Wed, 10 Feb 2021 17:25:51 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9f30b9ce624e9ec7d3a8264b15e4f9b6322a9ac9f1993a015f4c8d2976efea`  
		Last Modified: Wed, 10 Feb 2021 17:25:51 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7d0f03ef97b3b82f4ef1d19753faa9e1aad9688d00c91d6bd254e972a5d595`  
		Last Modified: Wed, 10 Feb 2021 17:25:51 GMT  
		Size: 67.2 KB (67204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129117c12de4cfe56c4efb4ab0c3ad95542ee63ef86db2c34cf1faa23b6b4b90`  
		Last Modified: Wed, 10 Feb 2021 17:25:48 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74f51c60182139a7b60e49f0afe4fb225303909e728132a5a60233ac104c39a`  
		Last Modified: Wed, 10 Feb 2021 17:25:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b5a645d2a1151a5e8fb3da40ac7073a1807bb258269ed43be7eb26003b403a`  
		Last Modified: Wed, 10 Feb 2021 17:26:07 GMT  
		Size: 180.0 MB (180035924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de31d2b4d83dd6be4051150af760d32b64d586e6009187c53636f61c11a7cf57`  
		Last Modified: Wed, 10 Feb 2021 17:25:49 GMT  
		Size: 3.7 MB (3666273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4df9fb2a09c926db724c2d8e0499eaf165e2a7397899e621a7fb977de662c25`  
		Last Modified: Wed, 10 Feb 2021 17:25:48 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
