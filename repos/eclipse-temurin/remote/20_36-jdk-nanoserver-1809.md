## `eclipse-temurin:20_36-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:022052db5443abcfad6dbacc09c3338034b609c287540806afb6c5160dcadf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `eclipse-temurin:20_36-jdk-nanoserver-1809` - windows version 10.0.17763.4252; amd64

```console
$ docker pull eclipse-temurin@sha256:25afa3e785c7350c2daf7b4e732cc4951618cafc3d11a8e04fafb46d63b019b3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305895501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec55d7ed4409db5456aa35d0b03253f129132a0ff317257f40a418efc0194ab`
-	Default Command: `["jshell"]`
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
# Wed, 12 Apr 2023 01:37:04 GMT
COPY dir:0bba24b8a26333fabbf995368b29d05051d1ff1f33d04d60afd33310da1fd9b4 in C:\openjdk-20 
# Wed, 12 Apr 2023 01:37:25 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Apr 2023 01:37:26 GMT
CMD ["jshell"]
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
	-	`sha256:a8c51129b872081d27401412f8a4cbd71d69552ddd07f826aa2206661429a7db`  
		Last Modified: Wed, 12 Apr 2023 09:44:26 GMT  
		Size: 195.3 MB (195253749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7569653c69e88f355755b234f886cdc59e31a9886cbdcc934b2495285281520c`  
		Last Modified: Wed, 12 Apr 2023 09:44:04 GMT  
		Size: 3.8 MB (3776958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c143b76a080e1768638485ee1f8710964f0dad6f4631c26127b93442c00417e`  
		Last Modified: Wed, 12 Apr 2023 09:44:03 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
