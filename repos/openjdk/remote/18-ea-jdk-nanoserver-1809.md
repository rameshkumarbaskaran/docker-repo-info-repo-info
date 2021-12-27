## `openjdk:18-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:9350e923a60e6dc0c24163c9ede3f65636e374986a414f66973bb7bfc8067fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `openjdk:18-ea-jdk-nanoserver-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull openjdk@sha256:40f1db275c6969c47efa72266230e44aed09862ae66ab9180690e77cc2176fa4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290477645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad6b1573f78ab27103589c98d2f9e88d354e9d67238e1bf0d39c9eb4972175c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 05:18:44 GMT
SHELL [cmd /s /c]
# Sat, 18 Dec 2021 07:11:41 GMT
ENV JAVA_HOME=C:\openjdk-18
# Sat, 18 Dec 2021 07:11:42 GMT
USER ContainerAdministrator
# Sat, 18 Dec 2021 07:11:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 18 Dec 2021 07:11:54 GMT
USER ContainerUser
# Mon, 27 Dec 2021 19:13:10 GMT
ENV JAVA_VERSION=18-ea+29
# Mon, 27 Dec 2021 19:13:43 GMT
COPY dir:4327435e3c54cd83f1b0d02e5d9913b8c2cd1f85f115f191272ebd2e60c28f88 in C:\openjdk-18 
# Mon, 27 Dec 2021 19:14:01 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 27 Dec 2021 19:14:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4c557aac927613dd487d7c04b01a8eeb8ad174693f61b14c8f4285f1db6afdd2`  
		Last Modified: Sat, 18 Dec 2021 06:13:05 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb09a08117aed517f83acd09c46245354fda9e1f94c432b6c5be4758bd11846a`  
		Last Modified: Sat, 18 Dec 2021 11:08:07 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9558b80b57be79d231423f31ff119a52bfde5373d41866669b3536cad1fe939`  
		Last Modified: Sat, 18 Dec 2021 11:08:07 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8f711c3cc04e41a513139b9dce135ea0dc407bb92c80b5fb14341e73eca8e7`  
		Last Modified: Sat, 18 Dec 2021 11:08:07 GMT  
		Size: 67.3 KB (67275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8203006c00a339abd7dace4c1b632bcbb99479c9cbd36cdf65f5ca4363d6872d`  
		Last Modified: Sat, 18 Dec 2021 11:08:05 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c67b12e4e392aac00a7065ddff771bdff1674f1b02cfd83ecc8d4c2238455d`  
		Last Modified: Mon, 27 Dec 2021 20:35:02 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23ae6af54a5284083c4a1bab142efeb7a39827896d24757d2863fba2634f75d`  
		Last Modified: Mon, 27 Dec 2021 20:35:21 GMT  
		Size: 183.9 MB (183938639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f7f8e337c9532c48120a1eda2de85a283ca698b41077e2712d92e651356b76`  
		Last Modified: Mon, 27 Dec 2021 20:35:06 GMT  
		Size: 3.6 MB (3560746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb433f27a7f77cfbdc8881be7f9722bb34b1fdb5f04c39aa482648e824bdccbe`  
		Last Modified: Mon, 27 Dec 2021 20:35:02 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
