## `eclipse-temurin:17-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:b00ae3e950bf5fbf4b5958ca748a89d1a462bc731f5f362f89b844e98c47be88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `eclipse-temurin:17-jdk-nanoserver-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull eclipse-temurin@sha256:4242e5c3e0c16fcf855820e1c453c75578c134817b07e6a1111b65fe1e9d56f3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293931377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc4f45c6c360bf1fc1a839ab0111d10a6e15a43a51712bddc21168760fe7e3e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Aug 2023 08:33:47 GMT
RUN Apply image 10.0.17763.4737
# Wed, 09 Aug 2023 23:39:50 GMT
SHELL [cmd /s /c]
# Thu, 31 Aug 2023 20:29:57 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Thu, 31 Aug 2023 20:29:57 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 31 Aug 2023 20:29:58 GMT
USER ContainerAdministrator
# Thu, 31 Aug 2023 20:30:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 31 Aug 2023 20:30:08 GMT
USER ContainerUser
# Thu, 31 Aug 2023 20:30:23 GMT
COPY dir:87d4868aeffb4665dc24a8514128e3f1a9351c7c90320c533fd29622fc9de6e2 in C:\openjdk-17 
# Thu, 31 Aug 2023 20:30:34 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 20:30:35 GMT
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
	-	`sha256:d579180f9e61898dea123c9b4c0edc42b464dfd0f1a7bc133ba5655d2e278339`  
		Last Modified: Thu, 31 Aug 2023 20:44:38 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d8d37e7bf677fa0f1e142ce3a584705d3dcedb61165384f14e741d85d54e3b`  
		Last Modified: Thu, 31 Aug 2023 20:44:38 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d18db2a934997819fa0aea584565d61b3eb49a1659fd37162c3f505085a63c`  
		Last Modified: Thu, 31 Aug 2023 20:44:38 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cf24a0a592732136360d0e90f43927b9a1838ff4cf624f7fbb41f749cce2fe`  
		Last Modified: Thu, 31 Aug 2023 20:44:36 GMT  
		Size: 68.4 KB (68399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e493056b4915706cebf68bed038b953c19967daae6657b4d89a828bc9cea09`  
		Last Modified: Thu, 31 Aug 2023 20:44:36 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40192037553de85046fdfe39f963da51007941a22a936181387869f771343f04`  
		Last Modified: Thu, 31 Aug 2023 20:44:54 GMT  
		Size: 185.7 MB (185726120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ed385d16695e84abe805f48cb63accd2fab78fbfeba6542df6fe751a375276`  
		Last Modified: Thu, 31 Aug 2023 20:44:37 GMT  
		Size: 3.7 MB (3670933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59416f60b32532c04d1e78c848e05c61a9d084fcbf6aa44596ea711f1496a380`  
		Last Modified: Thu, 31 Aug 2023 20:44:36 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
