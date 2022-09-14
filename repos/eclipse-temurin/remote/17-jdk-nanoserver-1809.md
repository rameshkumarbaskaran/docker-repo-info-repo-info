## `eclipse-temurin:17-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:b0bb7f54b76bfd5947725f8b83baf3d84849ee7ff2460e92108ebbd658153b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:17-jdk-nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull eclipse-temurin@sha256:e5acfd1b2f50d2789f192c4aa5ff8610ff15f765f3a67aa3b8d96f1a8d5b35eb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292423951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95de67e2e483959a430ff38541936fbbafb6f28df91d9f6a6277d7a290bb373`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 16:03:00 GMT
SHELL [cmd /s /c]
# Wed, 14 Sep 2022 16:21:28 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Wed, 14 Sep 2022 16:21:29 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 14 Sep 2022 16:21:29 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 16:21:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Sep 2022 16:21:40 GMT
USER ContainerUser
# Wed, 14 Sep 2022 16:21:54 GMT
COPY dir:de893fa6f4d02b385cd95015ab74e60b0c0c67a3785d10d2649390aedc7b2648 in C:\openjdk-17 
# Wed, 14 Sep 2022 16:22:09 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 14 Sep 2022 16:22:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:233f09b2a52487084f2cfb5e06dac2815651432c9d37c729582f59cfcf66b243`  
		Last Modified: Wed, 14 Sep 2022 16:47:12 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdc7267fe495d0cdf992be53b1fdd69c7c1ed0a3e2840762d8c5bb92c68a753`  
		Last Modified: Wed, 14 Sep 2022 16:52:48 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43f85722444dd97028b181a698b832b9c51cfcd6f12661ec22dec74858a8f3c`  
		Last Modified: Wed, 14 Sep 2022 16:52:48 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea208f743e3b8c0d1ba8973b583d6578c9c0cd9dfe02acce5e09a10df9c30bc`  
		Last Modified: Wed, 14 Sep 2022 16:52:48 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a00d33598c1ee2a4429cfa620e2bd5d1017c1c00b27c156856223f0c81bcbe3`  
		Last Modified: Wed, 14 Sep 2022 16:52:46 GMT  
		Size: 70.9 KB (70902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31aa2d6995a907d4a4fa5322a9d74f1c3f9548fe6a7f975a846b96aa5c6b603`  
		Last Modified: Wed, 14 Sep 2022 16:52:46 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed87ce0f271f443042fd98ca859f2114a68809d49baad2d1b262f1d032a0f06`  
		Last Modified: Wed, 14 Sep 2022 16:53:12 GMT  
		Size: 185.3 MB (185340978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733e205bcc70a09dfd78883952d6f6ef9cfd8e27d268c150e8e82751d62efc5b`  
		Last Modified: Wed, 14 Sep 2022 16:52:47 GMT  
		Size: 3.7 MB (3670979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e7fbaf4946709b25a45a8712905d325bd2340fd28f86d39ab8975fd97f4738`  
		Last Modified: Wed, 14 Sep 2022 16:52:46 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
