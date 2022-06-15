## `eclipse-temurin:18-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:3563a7864a7f1b5d7ad9cf6e31d0ea86d13e9c3cba46be8766fa0e9f5a16f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.768; amd64
	-	windows version 10.0.17763.3046; amd64

### `eclipse-temurin:18-jre-nanoserver` - windows version 10.0.20348.768; amd64

```console
$ docker pull eclipse-temurin@sha256:057a124f86ad18d275dd3dccb2ed57cecb9a717d11ee65f47ada04a2d91d381d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161169693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3c7d393b53788decb0b15fce7386f0c4c6fc7fe60252db901599de580cecbf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jun 2022 04:10:14 GMT
RUN Apply image 10.0.20348.768
# Wed, 15 Jun 2022 18:08:52 GMT
SHELL [cmd /s /c]
# Wed, 15 Jun 2022 18:13:52 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Wed, 15 Jun 2022 18:13:53 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 15 Jun 2022 18:13:54 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 18:14:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jun 2022 18:14:05 GMT
USER ContainerUser
# Wed, 15 Jun 2022 18:15:04 GMT
COPY dir:ba165d8363f6d3c715a5361167e7667ee35da551a187f89de48613c79c89ce98 in C:\openjdk-18 
# Wed, 15 Jun 2022 18:15:23 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:fca88290e1b048d74ec4e9d1548c4ec09dc3921f80285f39a186278fcaf2d86f`  
		Size: 118.0 MB (117976537 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:60cbdb7704dc53714205f32082d3faa20d7c93a53c40cb88f22581e85a2943fc`  
		Last Modified: Wed, 15 Jun 2022 19:13:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548edeb10e4bb743b69a9247eed1cce7535c1cf72730d3ad79120c94e4777af4`  
		Last Modified: Wed, 15 Jun 2022 19:22:52 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d433d0eb951a50620fd143ccc37bfdee174e986a9667e2130789f0cea31824`  
		Last Modified: Wed, 15 Jun 2022 19:22:52 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e674ac3369adee1947884c0a268657aaa682ee77094c2ab264a604a93f7ca116`  
		Last Modified: Wed, 15 Jun 2022 19:22:51 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0841f30e442afc7a145a17cd5534f47f77e30ed913efcb8c8d419a7dbb5c6509`  
		Last Modified: Wed, 15 Jun 2022 19:22:49 GMT  
		Size: 79.5 KB (79490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff48e0c8f74b8af8a996e4350347e31b641d89706e0a9e63e1ca85ddc68d6d7`  
		Last Modified: Wed, 15 Jun 2022 19:22:49 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4a1c13a9a9002388aa677eb932726f511958867a498508ca2ad014d5811b90`  
		Last Modified: Wed, 15 Jun 2022 19:26:40 GMT  
		Size: 43.0 MB (43047536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbb04bc94e997ca2e11991b4217e80b08580c805b44dee6b573d679414317dc`  
		Last Modified: Wed, 15 Jun 2022 19:26:31 GMT  
		Size: 60.7 KB (60718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jre-nanoserver` - windows version 10.0.17763.3046; amd64

```console
$ docker pull eclipse-temurin@sha256:ae0ae55c9677d339b84c396709b04a0664c89c4ebb501869f9270d8e756a0647
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149218958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b255fd5284798c5315a3f4c5155653959baedcf1de3699f8adaa620e82277f7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jun 2022 19:20:11 GMT
RUN Apply image 10.0.17763.3046
# Wed, 15 Jun 2022 17:30:58 GMT
SHELL [cmd /s /c]
# Wed, 15 Jun 2022 18:03:13 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Wed, 15 Jun 2022 18:03:14 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 15 Jun 2022 18:03:15 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 18:03:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jun 2022 18:03:27 GMT
USER ContainerUser
# Wed, 15 Jun 2022 18:08:26 GMT
COPY dir:ba165d8363f6d3c715a5361167e7667ee35da551a187f89de48613c79c89ce98 in C:\openjdk-18 
# Wed, 15 Jun 2022 18:08:43 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:d555a7e4de4dd775379d5c43c1419374bff7908670dc7444be5e8e8f386f3d26`  
		Size: 103.2 MB (103153235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92b4c385cd5cbb12fb09cb31c12b5e5de38cf7b380c8681286caac242c06d3ed`  
		Last Modified: Wed, 15 Jun 2022 18:22:11 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80401a436084179d205c8c414a595f0f5f88c6f2cef1f808b2adda75120906df`  
		Last Modified: Wed, 15 Jun 2022 19:06:19 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0ac3cf2eeddadcc0472d451142ef88b9951fa1080e0d5c711d01745bbe23e6`  
		Last Modified: Wed, 15 Jun 2022 19:06:18 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01935e2bd054ecaeddc9a097fe94873beb8b15d2849846336f56930aa195192c`  
		Last Modified: Wed, 15 Jun 2022 19:06:19 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f37aed99aa70d21c9042c2ef0fe8d5701bc48b3168293f4204e6e09e9a6bfe`  
		Last Modified: Wed, 15 Jun 2022 19:06:16 GMT  
		Size: 70.3 KB (70272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7565f6e8337ca088f94791a3a73f31ee22bd7c73a97d845575f38b434c10cb`  
		Last Modified: Wed, 15 Jun 2022 19:06:16 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9a92eafd4d7f34589781539af5d40de54aaefb3058f13b8e669948203c9ada`  
		Last Modified: Wed, 15 Jun 2022 19:13:33 GMT  
		Size: 43.0 MB (43047844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb52ee9d1c6beb2e45c623d2d975d977019b0630e4cc7c6218e778d41dba879`  
		Last Modified: Wed, 15 Jun 2022 19:12:50 GMT  
		Size: 2.9 MB (2941789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
