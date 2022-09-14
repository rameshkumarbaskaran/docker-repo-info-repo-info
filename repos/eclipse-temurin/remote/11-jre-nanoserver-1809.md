## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:b68450634a1b3ad8a94f6baa4bfaf137b9398b4a58f0189ef2a30a8084387841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull eclipse-temurin@sha256:9da8aa9e9b93867bde6007d573461df51d670ad2abd83496b34b43cd9560f044
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146377627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945c2917f5520450b3cb693210b189dcc38e503e61c64ea8fd0e34ef2522a1cd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 16:03:00 GMT
SHELL [cmd /s /c]
# Wed, 14 Sep 2022 16:12:05 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 14 Sep 2022 16:12:06 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 14 Sep 2022 16:12:07 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 16:12:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Sep 2022 16:12:17 GMT
USER ContainerUser
# Wed, 14 Sep 2022 16:16:40 GMT
COPY dir:b650de7fc0e3b0755f26a7348890f8f5a4e1b6ed07c2d2df82fc07e7eb59e165 in C:\openjdk-11 
# Wed, 14 Sep 2022 16:16:55 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:233f09b2a52487084f2cfb5e06dac2815651432c9d37c729582f59cfcf66b243`  
		Last Modified: Wed, 14 Sep 2022 16:47:12 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0cd1b11fcd5c6501385ccbf55adda353b30907a4f34fa696e8ba9eb57fe72`  
		Last Modified: Wed, 14 Sep 2022 16:49:51 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f53381a52e06d5ca3814b41e1c956eeeda1a756850ec94c56924987e956dd14`  
		Last Modified: Wed, 14 Sep 2022 16:49:51 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81367e02484ec9fdab571c6ad7be9463a7eb5d39a07b7d0204b16acb30e2e6af`  
		Last Modified: Wed, 14 Sep 2022 16:49:51 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56ea5adb1e9aa6a064aa275c4d5aee7b97d797faaa27b0faa4ff45d8e39bbab`  
		Last Modified: Wed, 14 Sep 2022 16:49:49 GMT  
		Size: 76.0 KB (76011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b9ea271df35fcd3360936af19dc706b939d9ed5f8894ccf26f73c1037ea461`  
		Last Modified: Wed, 14 Sep 2022 16:49:49 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d68789663324dd75ae70871e7ee009a7dca14aba7c02e84756bdccfe58b54aa`  
		Last Modified: Wed, 14 Sep 2022 16:51:08 GMT  
		Size: 42.9 MB (42914621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7f3d2d9145a8253a3f36c0807dd548961ab7fa0bfc8488cc148862f4d1edb1`  
		Last Modified: Wed, 14 Sep 2022 16:51:00 GMT  
		Size: 47.1 KB (47130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
