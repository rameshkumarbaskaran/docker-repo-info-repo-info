## `eclipse-temurin:20_36-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:6bf1934c10f5aa790e088a2e52a127bc6882e43747ba03cfc6a8833dfe1509a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `eclipse-temurin:20_36-jre-nanoserver-1809` - windows version 10.0.17763.4252; amd64

```console
$ docker pull eclipse-temurin@sha256:2307e59c9fe10e9deed4150e8edeeee4f571f32d7a8175354b0d65a1083179eb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155745321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21d098c25075263097966b4bf95bef248bb330b7019ec02df991880a8c25997`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Tue, 11 Apr 2023 23:45:41 GMT
SHELL [cmd /s /c]
# Wed, 12 Apr 2023 01:36:30 GMT
ENV JAVA_VERSION=jdk-20+36
# Wed, 12 Apr 2023 01:36:31 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 12 Apr 2023 01:36:31 GMT
USER ContainerAdministrator
# Wed, 12 Apr 2023 01:36:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Apr 2023 01:36:49 GMT
USER ContainerUser
# Wed, 12 Apr 2023 01:41:56 GMT
COPY dir:88253b833ff2634324ea23b2cdfd627ca2e30273c5f29426251a8626a4f6baa7 in C:\openjdk-20 
# Wed, 12 Apr 2023 01:42:10 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:af799fb2ff133c89311c6a42d34b8cb6c9b11d775f52e04ab08389d05e64ed1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:10 GMT  
		Size: 106.8 MB (106788951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1db438f20b81fe0c031e4e3eee58d278fba7258d01057ff18964cccf70d41c`  
		Last Modified: Wed, 12 Apr 2023 00:52:38 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ce5de1c6c3e182e390fbd587888ada347a6c8acdb9c36d0acb82b56f58f723`  
		Last Modified: Wed, 12 Apr 2023 09:44:06 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2176ad1b2d01a0c49cfafd513e39dfdcb902e1434a6575bf7d726c547e71a3`  
		Last Modified: Wed, 12 Apr 2023 09:44:05 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa7cd546e7dbbb9155483c115c8a501d58faf398c62d3162d3b631972d27d00`  
		Last Modified: Wed, 12 Apr 2023 09:44:05 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75552b77c71ecbb7dba9a11bfc508d63227ea66c2866e7c061a8885537ad56f`  
		Last Modified: Wed, 12 Apr 2023 09:44:04 GMT  
		Size: 69.0 KB (69018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdaa54362a8c4616f7807a0e03039c0d746f0118e5de1c97a087c723978ec78`  
		Last Modified: Wed, 12 Apr 2023 09:44:03 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4ce5059d46404cf2912424885d258a872ac13559ba0b0a259e247a5dca94b6`  
		Last Modified: Wed, 12 Apr 2023 09:45:30 GMT  
		Size: 45.7 MB (45738938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cbe07d284b83f45ed7c38496dad4a476250118589c282cbab1400d2bc5e14b`  
		Last Modified: Wed, 12 Apr 2023 09:45:21 GMT  
		Size: 3.1 MB (3142729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
