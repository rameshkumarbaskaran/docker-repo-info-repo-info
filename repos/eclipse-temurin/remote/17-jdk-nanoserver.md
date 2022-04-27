## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:10c209f45592f0891a869430ba80f3a647d28b664829b46f7d62e0fd1a8f2687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.643; amd64
	-	windows version 10.0.17763.2803; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.643; amd64

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

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.17763.2803; amd64

```console
$ docker pull eclipse-temurin@sha256:57d195c1005cb51a42b6c3964766d30d0e0973a03dbf5c0eac741de5b077ec07
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (292010181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cdadef3c0738f7cfbf8ba408f006ec5aca5082f1db6b6b363b8714e48791cf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 15:16:11 GMT
SHELL [cmd /s /c]
# Wed, 27 Apr 2022 18:32:01 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Wed, 27 Apr 2022 18:32:02 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 27 Apr 2022 18:32:02 GMT
USER ContainerAdministrator
# Wed, 27 Apr 2022 18:32:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 27 Apr 2022 18:32:10 GMT
USER ContainerUser
# Wed, 27 Apr 2022 18:32:25 GMT
COPY dir:79e149bb8ddfd2a6f3a6975343033743c253d84c3b058ff83fe3162d456d08dd in C:\openjdk-17 
# Wed, 27 Apr 2022 18:32:38 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 27 Apr 2022 18:32:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ea4009814dceb50337c66614a6008cfc2fb73ce53e62162bce071ef6ea1adf2d`  
		Last Modified: Wed, 13 Apr 2022 15:58:06 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d34faf5e5831a403b144b0687c9e5ee8a42e8804cc799431fa71b88d0642a48`  
		Last Modified: Wed, 27 Apr 2022 19:49:49 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60210357460062d2100fd8821e95c3c372622db4d3a4b38c392868a4109fe0f4`  
		Last Modified: Wed, 27 Apr 2022 19:49:49 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6a35fa21e7b0c2a147687eef2f70e4c428c84feb448fdcdb642672a4548542`  
		Last Modified: Wed, 27 Apr 2022 19:49:49 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31effde11f17e4d584a40e3c2ecb07f08869396338dcbbdc408db95dcced2f2c`  
		Last Modified: Wed, 27 Apr 2022 19:49:46 GMT  
		Size: 76.4 KB (76353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dec76f1c6060bed7f93b40161130470b973597a6c49543bb56589811a0cb712`  
		Last Modified: Wed, 27 Apr 2022 19:49:46 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bccf06c75b8e99593a12f1ac76ebcd972be960efef1288d742c06828625b4c8f`  
		Last Modified: Wed, 27 Apr 2022 19:50:07 GMT  
		Size: 185.2 MB (185205680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33cd690c0ff9462963d00ef7ad2760ca64e194dd0f519914741aed36f54ccce`  
		Last Modified: Wed, 27 Apr 2022 19:49:50 GMT  
		Size: 3.6 MB (3625249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1874b6918cf8cf476895bcda29d073706c22c1e95d1b126a8e496fa4d141a20`  
		Last Modified: Wed, 27 Apr 2022 19:49:46 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
