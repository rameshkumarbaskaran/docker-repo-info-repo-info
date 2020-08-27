## `openjdk:16-nanoserver`

```console
$ docker pull openjdk@sha256:e67003709e81a3d5f8b2ea1f4eef4698b137ce1e95ec199bc3dc777ba84ef250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `openjdk:16-nanoserver` - windows version 10.0.17763.1397; amd64

```console
$ docker pull openjdk@sha256:b6ebc7ca5de8f479811b7c2ed710e5779d2b5aecd3c0b3368e4d743a4193184c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.8 MB (296800689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a5d1bc10f7f62a126bb1dfffe2da4f382b6559e9bf6a3f5b476e9612e156c5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:28:05 GMT
SHELL [cmd /s /c]
# Wed, 12 Aug 2020 15:28:06 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 12 Aug 2020 15:28:06 GMT
USER ContainerAdministrator
# Wed, 12 Aug 2020 15:28:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 12 Aug 2020 15:28:22 GMT
USER ContainerUser
# Thu, 27 Aug 2020 22:18:55 GMT
ENV JAVA_VERSION=16-ea+13
# Thu, 27 Aug 2020 22:19:36 GMT
COPY dir:6614039b29dcb19416629ed6cc243566f4c35add0cbd22ea3729486f939ba552 in C:\openjdk-16 
# Thu, 27 Aug 2020 22:20:03 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Thu, 27 Aug 2020 22:20:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1c7c341c7a3d0c7b6e849b6faec560815682d07ce87df2e4d1e83f928aab306b`  
		Last Modified: Wed, 12 Aug 2020 16:10:21 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4ff90b84cb0e951da0f399342768862ac8c294fbe71e80d787a60d9cc2c7b5`  
		Last Modified: Wed, 12 Aug 2020 16:10:20 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f566429948e6233b746b6d219e57703486a6f2f00910b8e1842ff9920d1834e1`  
		Last Modified: Wed, 12 Aug 2020 16:10:20 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4bcc2b175dfe1adf68a872a4fa40033320f09b67b59f3dbf35cae4783189d4`  
		Last Modified: Wed, 12 Aug 2020 16:10:20 GMT  
		Size: 65.9 KB (65918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca4105c8d6a5159a2ffd6904f118076cb11506891820a04656978435fd29bad`  
		Last Modified: Wed, 12 Aug 2020 16:10:17 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa2129a62e2f4bd8c506065df6b911e59581a3a007b6c1a7438882ea4117caf`  
		Last Modified: Thu, 27 Aug 2020 22:25:28 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323596218a3013fa14bbddfff8a527049b40367223ed4ba46f76708eddad9779`  
		Last Modified: Thu, 27 Aug 2020 22:25:47 GMT  
		Size: 192.2 MB (192225833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50caaa6d6c46898ee213d69657a13baa7a573b9dda047bb6bf4658bd1256d04c`  
		Last Modified: Thu, 27 Aug 2020 22:25:29 GMT  
		Size: 3.5 MB (3518680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f810c1c6dd5331a26257fb941e63deb846e2431411ac2a07125515dbe85872`  
		Last Modified: Thu, 27 Aug 2020 22:25:28 GMT  
		Size: 928.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
