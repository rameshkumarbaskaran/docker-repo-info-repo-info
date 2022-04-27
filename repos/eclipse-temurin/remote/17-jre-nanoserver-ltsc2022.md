## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:f586d9a96818322c9d67baa316b4fdb31573781fd0c8d5fbfe28295d67b99ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.643; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.643; amd64

```console
$ docker pull eclipse-temurin@sha256:1e04916e5e3a0997debc9ac10e091b53a91af79ae4ece9428200a51f66c62471
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160866515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976c2d33eb97bff05557b60466f1d770599daa0d104a50f57cd72249d620b0e0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 27 Apr 2022 18:39:38 GMT
COPY dir:c21630f3252a44226ea19120d87b000e49aedb9d546bbac0f6424fd80f37c64d in C:\openjdk-17 
# Wed, 27 Apr 2022 18:39:49 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:a4a1355986d584ab7a369001a007422730ffd15f80e5b507e4e0c96b982348da`  
		Last Modified: Wed, 27 Apr 2022 20:03:40 GMT  
		Size: 43.1 MB (43123462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82c063814d7d45f3e3759403d1865c4fdcea88c19b756c94185ea9bacee15dc`  
		Last Modified: Wed, 27 Apr 2022 20:02:52 GMT  
		Size: 74.4 KB (74364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
