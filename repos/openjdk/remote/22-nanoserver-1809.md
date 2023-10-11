## `openjdk:22-nanoserver-1809`

```console
$ docker pull openjdk@sha256:26e528436a38cf0829a230b5cf55296bc4375fe9917ad308e983c490685da4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `openjdk:22-nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull openjdk@sha256:63b31fe5cbd80c3544f6273ac800668c4c91b955a442a1d9d5d95f0f37233c94
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.5 MB (307521636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3671cde7c18ab0ef9d6f80daa130f76a479aa8fb0ee223d556d11a0b68430a00`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 01:39:37 GMT
SHELL [cmd /s /c]
# Wed, 11 Oct 2023 03:54:23 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 11 Oct 2023 03:54:24 GMT
USER ContainerAdministrator
# Wed, 11 Oct 2023 03:54:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 11 Oct 2023 03:54:36 GMT
USER ContainerUser
# Wed, 11 Oct 2023 03:54:37 GMT
ENV JAVA_VERSION=22-ea+18
# Wed, 11 Oct 2023 03:54:51 GMT
COPY dir:cdb676c7e47998ad35b8028b63314ad3ca3556dd433bebfc48557cc58d5a880e in C:\openjdk-22 
# Wed, 11 Oct 2023 03:55:02 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 11 Oct 2023 03:55:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c11581d9ee9ea19d58c6cbb415dd809a51b56502169a7a5b301da76d79f63b`  
		Last Modified: Wed, 11 Oct 2023 03:57:05 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f7d94044a293783b6667a23790497e452737d17d7221e9fcf940fd19c4f9c6`  
		Last Modified: Wed, 11 Oct 2023 03:57:04 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9d706d8cea409c86409f061201a999c5fdfc900eeb9cd2c8d7c214bd462f3b`  
		Last Modified: Wed, 11 Oct 2023 03:57:04 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c93fa899ae2056b59330f20c6e4a27ec6737929f17b7fa5a275baca12f8b1eb`  
		Last Modified: Wed, 11 Oct 2023 03:57:04 GMT  
		Size: 70.3 KB (70294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f049fc80168b8466bfbf3fd6b202ac8273bc9bd873e579290c2df3cb795a69b`  
		Last Modified: Wed, 11 Oct 2023 03:57:02 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d55430d045b4402c0223105b66827b9983a534cfd26822988c4f6441641545`  
		Last Modified: Wed, 11 Oct 2023 03:57:02 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b39aa76307c99ed249dde5e497f36b9255a443ae8e489f55eda56cf4a7bfdd8`  
		Last Modified: Wed, 11 Oct 2023 03:57:21 GMT  
		Size: 199.1 MB (199139832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33de0375c15e9460cc55b67810b286a02cd4ac3528dfa00852fe8a7b5ec4648d`  
		Last Modified: Wed, 11 Oct 2023 03:57:03 GMT  
		Size: 3.8 MB (3840640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a5d067a31b55ecbadae5039e9cbc5a132003e32dbef3fbcbf5b74b44dff6f9`  
		Last Modified: Wed, 11 Oct 2023 03:57:02 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
