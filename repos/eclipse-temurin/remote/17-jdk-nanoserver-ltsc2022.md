## `eclipse-temurin:17-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0b8fc4dc96580ebfeb0913d7c9fab2f2e530439d3d08db207e926c6a71511e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.643; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.643; amd64

```console
$ docker pull eclipse-temurin@sha256:7c62f0ae25909d90927cd50016cf055d0c54c976e5d7d3f1ec81a190dd65b932
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302934051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c077f0ab98e443ab1ea11682f85a4ef19e06bafde870d505ff08e164535c378`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 03 Apr 2022 05:29:07 GMT
RUN Apply image ltsc2022-amd64
# Wed, 13 Apr 2022 15:47:59 GMT
SHELL [cmd /s /c]
# Wed, 27 Apr 2022 18:38:45 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Wed, 27 Apr 2022 18:38:46 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 27 Apr 2022 18:38:47 GMT
USER ContainerAdministrator
# Wed, 27 Apr 2022 18:38:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 27 Apr 2022 18:38:54 GMT
USER ContainerUser
# Wed, 27 Apr 2022 18:39:09 GMT
COPY dir:79e149bb8ddfd2a6f3a6975343033743c253d84c3b058ff83fe3162d456d08dd in C:\openjdk-17 
# Wed, 27 Apr 2022 18:39:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 27 Apr 2022 18:39:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5ee98801bdad72bc36678d072c89f7dd482fee29086c1d9c8ad6ff0cb5afa385`  
		Size: 117.6 MB (117579416 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:924a7c42e559a85c0bc74dbb028ddeee43fe67b0f59c81c60cbda0082e0e3ae5`  
		Last Modified: Wed, 13 Apr 2022 16:38:31 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f57f43d219f1c95396fedae5093ac63dc308b65db510943a43b23d9b4202ba`  
		Last Modified: Wed, 27 Apr 2022 19:59:15 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b3473f8f5fdfc3ffbbc49afc8af4c9a5e68cec7febbeabda7669ca3de725cf`  
		Last Modified: Wed, 27 Apr 2022 19:59:15 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88386b35c8533b47ba8f3a9ec833f2e24e80475398d9addcef603325296cc3a7`  
		Last Modified: Wed, 27 Apr 2022 19:59:15 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a95f756bdb8764145cc08d95e652cec6a4d603d3550a592b94f08be1cdd80d3`  
		Last Modified: Wed, 27 Apr 2022 19:59:13 GMT  
		Size: 83.6 KB (83593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9dc6498186401fee05693a92d6957dde27531069ce8dbf5f1fa965454d4869`  
		Last Modified: Wed, 27 Apr 2022 19:59:13 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56502ec350a7f666ce319c5887685ad3d1ffff5fdf435cdef3bf054ef7ab78f`  
		Last Modified: Wed, 27 Apr 2022 20:02:37 GMT  
		Size: 185.2 MB (185177075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28a192f6eed1b8569ea44b9dee71081873addd626787943c16a634d3397a847`  
		Last Modified: Wed, 27 Apr 2022 19:59:13 GMT  
		Size: 87.1 KB (87124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70bcabddbeb3a5b35d23c042a41c5985041a11d500ee6629fd76d89a91dfe30`  
		Last Modified: Wed, 27 Apr 2022 19:59:13 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
