## `openjdk:16-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:c59e1b54c904bceab6020c36059b73cc9e9897bc3e408ed164ed658d8add8d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `openjdk:16-jdk-nanoserver` - windows version 10.0.17763.1757; amd64

```console
$ docker pull openjdk@sha256:9cc3bc856ee756a9acf325cc645c04961a3c7ecddb26da225e8c4149ee576da6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285178335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f92f642bf5a2cfffbcfeea97d83ed5322a9e7822e69b79455f502793bb81609`
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
# Fri, 12 Feb 2021 23:23:44 GMT
COPY dir:03c380a356e8b0fa2d413bbd7f8427b40b2c6808fd016e7b77d87b6b5da6487b in C:\openjdk-16 
# Fri, 12 Feb 2021 23:24:00 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 12 Feb 2021 23:24:01 GMT
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
	-	`sha256:90d97e967c863c3ccfc3d1f5c638ccbe4dec183624db1b3e09ccafc9efa5ac99`  
		Last Modified: Fri, 12 Feb 2021 23:38:49 GMT  
		Size: 180.0 MB (180032626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e93f23109a78b7cffec285eac52ac05cb101dbc1a5b25a74be3bed68dd8b736`  
		Last Modified: Fri, 12 Feb 2021 23:38:33 GMT  
		Size: 3.7 MB (3665772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2268d05a07356779c97a19147ad642bc94428898fa720cb62aa4c33a8cbd0c`  
		Last Modified: Fri, 12 Feb 2021 23:38:29 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
