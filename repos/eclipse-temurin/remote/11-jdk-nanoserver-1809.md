## `eclipse-temurin:11-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:f28ce725de323bc0479c7d58fb68b09bfd3b65cdfedfe671416bfa128c3755aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `eclipse-temurin:11-jdk-nanoserver-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull eclipse-temurin@sha256:533089ec3b6af6e2179c16e6298207968f4ad13c4624529a6054ecfc1a9a3c29
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297721294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395a5bba10b1778f00e8ce9de335b10c8e32f2b1dc3243763db588e356925b8f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Aug 2023 08:33:47 GMT
RUN Apply image 10.0.17763.4737
# Wed, 09 Aug 2023 23:39:50 GMT
SHELL [cmd /s /c]
# Thu, 31 Aug 2023 20:20:21 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Thu, 31 Aug 2023 20:20:21 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 31 Aug 2023 20:20:22 GMT
USER ContainerAdministrator
# Thu, 31 Aug 2023 20:20:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 31 Aug 2023 20:20:31 GMT
USER ContainerUser
# Thu, 31 Aug 2023 20:20:45 GMT
COPY dir:bc17122f89ccac6825b72157f71faf8ee914101def60109a37803e17ec7fe7f6 in C:\openjdk-11 
# Thu, 31 Aug 2023 20:20:58 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 20:20:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86fab75eb466cadf89d853682179b3b57eba9fe28c78041dd52bced81e18a627`  
		Last Modified: Tue, 08 Aug 2023 17:55:54 GMT  
		Size: 104.5 MB (104459386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7e08c5247c8c7d832882da17ac85015e9dd4d4dfc9e4114fc14746eb2abded`  
		Last Modified: Thu, 10 Aug 2023 00:21:01 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0400cdde7fcf7a26c0052c9d54e18321cc24a8e7a901c3cedf454510c2df6f36`  
		Last Modified: Thu, 31 Aug 2023 20:41:55 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d471948f58e97575944c29155e8d2657969364a0baacbb17575c067f8ec113a6`  
		Last Modified: Thu, 31 Aug 2023 20:41:55 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe20d26742869dd1f442a34b7dbe8639f578c9d6daedac7316870e19dabbc45`  
		Last Modified: Thu, 31 Aug 2023 20:41:55 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbc2c0338d03cec2b363c2914c6cfe38f2ac1f3a253a02b8435336ebac71b53`  
		Last Modified: Thu, 31 Aug 2023 20:41:53 GMT  
		Size: 71.2 KB (71233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d47a25ff5e1d6aa0ff92cb9ca26b321a6dc6d779390f18374c3218e4f109b23`  
		Last Modified: Thu, 31 Aug 2023 20:41:53 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a242761134f0fd53e07aa4b1e63e3aba2d0303f09b5e0b1e39527c361e0bce9`  
		Last Modified: Thu, 31 Aug 2023 20:42:11 GMT  
		Size: 193.1 MB (193100104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ebc6da128c160c0302f89f4031f7ea4995307ae5bc6856dbf5eea66c06d518`  
		Last Modified: Thu, 31 Aug 2023 20:41:53 GMT  
		Size: 83.7 KB (83660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5048d08b06a63ab028143ffe1764a254f27218df6594ba1c6481c051ea28d2`  
		Last Modified: Thu, 31 Aug 2023 20:41:53 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
