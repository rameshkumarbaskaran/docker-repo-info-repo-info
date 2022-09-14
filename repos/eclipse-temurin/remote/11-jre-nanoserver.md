## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:187cf18d5689d78fe53cc0d4f841b7506f763a9d433a3442ec5a5539ebb28531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:8d3edd37ec8662fbdcd34f0d3191b7a43c3b602f934ebe57ee59d248326f8468
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161192303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f733f778c6c9000a61b684974491d23afedae8e126be8c8b1cd1d69b37fd3b60`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Sep 2022 20:11:22 GMT
RUN Apply image 10.0.20348.1006
# Wed, 14 Sep 2022 16:38:20 GMT
SHELL [cmd /s /c]
# Wed, 14 Sep 2022 16:39:41 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 14 Sep 2022 16:39:42 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 14 Sep 2022 16:39:42 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 16:39:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Sep 2022 16:39:53 GMT
USER ContainerUser
# Wed, 14 Sep 2022 16:40:41 GMT
COPY dir:b650de7fc0e3b0755f26a7348890f8f5a4e1b6ed07c2d2df82fc07e7eb59e165 in C:\openjdk-11 
# Wed, 14 Sep 2022 16:40:54 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:09629875cd6ee57fa551626fa2963d8b54718ba9acbf28e7cb5d684a9cb754d7`  
		Size: 118.1 MB (118131331 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:07f30e2ceaa03f6ac7b6e6f319083288f48d1fa2a61f36f51f516da241496976`  
		Last Modified: Wed, 14 Sep 2022 16:57:28 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e9874cfb1290b2d18c9beffbfd99b9d1e09f8af04b374db214974968038e3e`  
		Last Modified: Wed, 14 Sep 2022 16:58:10 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ec2fe2f33ab50e9fa4932ea36425b3d16e951341beb15e4b1c762c87b2f44f`  
		Last Modified: Wed, 14 Sep 2022 16:58:10 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b9290f6a2ecdeccefa5fc537a9bad68e44802e0418c0db24ac05d1db414386`  
		Last Modified: Wed, 14 Sep 2022 16:58:10 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f528201d81349fe0b28a43ec78fab2f3b0735cdd9cfa89dc61faf9c8799738`  
		Last Modified: Wed, 14 Sep 2022 16:58:07 GMT  
		Size: 79.8 KB (79762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3285b65edefe11e2a40bacbc70c3cc99083205447f036f436c4aabdb3b0b169a`  
		Last Modified: Wed, 14 Sep 2022 16:58:07 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be1e89da0ea6c27e50f9e2a0f3f9141077e0a247a7ba3b46c7c7e3a5555b37`  
		Last Modified: Wed, 14 Sep 2022 16:58:47 GMT  
		Size: 42.9 MB (42913905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f3991beceb88a8a035e82fe4eafb6f5020abe075d9d8cbabe002acf23de075`  
		Last Modified: Wed, 14 Sep 2022 16:58:40 GMT  
		Size: 62.1 KB (62087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.3406; amd64

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
