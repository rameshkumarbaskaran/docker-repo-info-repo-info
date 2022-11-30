## `openjdk:20-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:9aefe981a4ea54d5f570c07ac608769a3ca93ba8d8297f79c6a51ba7ef54d45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `openjdk:20-ea-jdk-nanoserver` - windows version 10.0.17763.3650; amd64

```console
$ docker pull openjdk@sha256:12a7001d358c86872595927f27b28fb5862439d34266830485ca3ef8ec7af943
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303482970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f77b095493fd50b22742af41471c0f7b69ae0c748e37d6621d8598914085fb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Tue, 08 Nov 2022 18:36:25 GMT
SHELL [cmd /s /c]
# Wed, 09 Nov 2022 17:26:48 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 09 Nov 2022 17:26:49 GMT
USER ContainerAdministrator
# Wed, 09 Nov 2022 17:27:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Nov 2022 17:27:07 GMT
USER ContainerUser
# Wed, 30 Nov 2022 21:18:44 GMT
ENV JAVA_VERSION=20-ea+25
# Wed, 30 Nov 2022 21:19:01 GMT
COPY dir:f30087c42a3e58e962b9f9476bcc80ec1ac216562c7f71a6195860f6e614259c in C:\openjdk-20 
# Wed, 30 Nov 2022 21:19:34 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 30 Nov 2022 21:19:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e8f4bb4b79b67857c1e4ac5c66026fd5ff5badbde5a8b59b11251b02699586`  
		Last Modified: Tue, 08 Nov 2022 19:44:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5380ecadb3b5072bd5e7cf41fa446b5ae89ef7d71fde34772d7b32062aca954b`  
		Last Modified: Wed, 09 Nov 2022 17:37:09 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de19002dcea365821038023716e28374a8210ac45b5a63b539639130ad9b6bd8`  
		Last Modified: Wed, 09 Nov 2022 17:37:08 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc05d65ddfbc35592002f4ae7726cad3fa9b8777ac1f0cbb66bad8963c18cc7`  
		Last Modified: Wed, 09 Nov 2022 17:37:08 GMT  
		Size: 74.7 KB (74716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0517802e30312d5724623bf6cc9fe338f7330d522b267fad48ae4f85da52072`  
		Last Modified: Wed, 09 Nov 2022 17:37:06 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e56d1f13384552e2b6c3abe657f434c62c2e0dc36b3c9a90cbf75353c00855b`  
		Last Modified: Wed, 30 Nov 2022 21:23:03 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fb313d8dce0d6aa499ab3babc853bd6429bbf959a964e8f15d3f82500375bd`  
		Last Modified: Wed, 30 Nov 2022 21:23:25 GMT  
		Size: 192.9 MB (192896354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c9c00e89ced9df602b98b1de4220e0ba78a54df69479006f50d87cf280daef`  
		Last Modified: Wed, 30 Nov 2022 21:23:04 GMT  
		Size: 3.8 MB (3781964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f0d4c14894d8f405e5a579909717aa8227b5df1f4c6beec6f304ad546b0376`  
		Last Modified: Wed, 30 Nov 2022 21:23:03 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
