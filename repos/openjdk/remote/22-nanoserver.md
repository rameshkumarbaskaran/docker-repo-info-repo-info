## `openjdk:22-nanoserver`

```console
$ docker pull openjdk@sha256:4de2428ba9affd4bf36c89316c78ca332d3d8a99cb43abf30498069f3461546e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `openjdk:22-nanoserver` - windows version 10.0.17763.4499; amd64

```console
$ docker pull openjdk@sha256:a6ba99c1c5715433c8acf22483567db7785838a23c0a3e5e7bb42609e521a147
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307102387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74ab1eb874f3cb16ffc1f955fe14e6f9aed5e0f5308ef48e9a50fa2f6477644`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jun 2023 12:28:32 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 17:41:42 GMT
SHELL [cmd /s /c]
# Wed, 14 Jun 2023 20:28:06 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 14 Jun 2023 20:28:06 GMT
USER ContainerAdministrator
# Wed, 14 Jun 2023 20:28:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Jun 2023 20:28:16 GMT
USER ContainerUser
# Wed, 14 Jun 2023 20:28:17 GMT
ENV JAVA_VERSION=22-ea+1
# Wed, 14 Jun 2023 20:28:32 GMT
COPY dir:b92259b80436bb1fd33a07a598f496a2bb18bd238b995c9b8b4c25abf0b81a2d in C:\openjdk-22 
# Wed, 14 Jun 2023 20:28:46 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 14 Jun 2023 20:28:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:234d39d9b188e7f36d5a77b0d54990ea826551314b6703c83aef3ef20b1a7050`  
		Last Modified: Tue, 13 Jun 2023 19:06:23 GMT  
		Size: 104.4 MB (104397895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2364e413270ecc5b57d2596b092fb57b828229b59e810d9f345fc0d31ca535d`  
		Last Modified: Wed, 14 Jun 2023 18:26:46 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816e92368fa87f9798749d97162f386f464e5cb0e4a668b35ac6929b5f9bdbab`  
		Last Modified: Wed, 14 Jun 2023 20:35:15 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d241a7335cf0716c38d3ab576802c34648d69d25e847638aa7db2132e881461e`  
		Last Modified: Wed, 14 Jun 2023 20:35:16 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6d759053b47bb836ae8319abce7846d93cfdf210fb3e4b0bcce271fbda6d9e`  
		Last Modified: Wed, 14 Jun 2023 20:35:15 GMT  
		Size: 74.6 KB (74612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3005cad1749dc64b4a46eb5a441e05083078d3075dbdb1cac2beba0044199668`  
		Last Modified: Wed, 14 Jun 2023 20:35:13 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a453d86cdc3281ec4b29e8b1e441d6de6f4d5e4c8970900c73852bc3e4b6059`  
		Last Modified: Wed, 14 Jun 2023 20:35:13 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b936818de9e53df2d65434a2125eddc90bde0cad7f8f40ae98f44fdf69aabc`  
		Last Modified: Wed, 14 Jun 2023 20:35:34 GMT  
		Size: 198.8 MB (198843730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29efe3e512d2f9a6943a7fc2548e7e2b07054231962b270b4633f0b9ea7d686c`  
		Last Modified: Wed, 14 Jun 2023 20:35:14 GMT  
		Size: 3.8 MB (3779679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ac55835e1dd73fe827d20a3b25b97f8be24fd1ebc8e6ad93ed848978ce6ea4`  
		Last Modified: Wed, 14 Jun 2023 20:35:13 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
