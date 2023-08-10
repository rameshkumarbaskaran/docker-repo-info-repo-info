## `openjdk:22-ea-9-nanoserver-1809`

```console
$ docker pull openjdk@sha256:f1c47ecd1ebffa482a0c632b992c3b89f58dc7f5faf75cbc46291df3bec05010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `openjdk:22-ea-9-nanoserver-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull openjdk@sha256:b7854e25104c6cac8a9e69473a9b8266384a4e27df65ebc4aadc9d60c3243a1f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.3 MB (307279543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be1b2e400a99979f6e41b4f708d7f3958b30e2458fe04e43632d6a505bcb9a07`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Aug 2023 08:33:47 GMT
RUN Apply image 10.0.17763.4737
# Wed, 09 Aug 2023 23:39:50 GMT
SHELL [cmd /s /c]
# Thu, 10 Aug 2023 02:42:08 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 10 Aug 2023 02:42:09 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 02:42:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 10 Aug 2023 02:42:20 GMT
USER ContainerUser
# Thu, 10 Aug 2023 02:42:20 GMT
ENV JAVA_VERSION=22-ea+9
# Thu, 10 Aug 2023 02:42:34 GMT
COPY dir:6a23f2ebf681c4c32ab25d2a9e21b8cc95ce17229ce3a9322148fc1dab64b4fc in C:\openjdk-22 
# Thu, 10 Aug 2023 02:42:48 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 10 Aug 2023 02:42:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86fab75eb466cadf89d853682179b3b57eba9fe28c78041dd52bced81e18a627`  
		Last Modified: Tue, 08 Aug 2023 17:55:54 GMT  
		Size: 104.5 MB (104459386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7e08c5247c8c7d832882da17ac85015e9dd4d4dfc9e4114fc14746eb2abded`  
		Last Modified: Thu, 10 Aug 2023 00:21:01 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a07a6ee55409326d8105cc13d850b1705bbe4498575cf2e27bc34e78a1b5063`  
		Last Modified: Thu, 10 Aug 2023 02:50:16 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f896f4ed09b9390bcd098f89bb4624ae91e82cf7a9c4588ecdeeaa28378701`  
		Last Modified: Thu, 10 Aug 2023 02:50:15 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa6961892f2fba93ceeaf5806dc38793f041309ff787a61ccbd94e178ffd4af`  
		Last Modified: Thu, 10 Aug 2023 02:50:16 GMT  
		Size: 71.1 KB (71084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d01d10dd6ecb83bb10dfbaee0c9743aa78c0fb19d3da95691428a5cb7c9e078`  
		Last Modified: Thu, 10 Aug 2023 02:50:13 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571ffa87c0cd2e6038f7a4d4d5ebb705ad719b067e93a124947f96a48a019c7c`  
		Last Modified: Thu, 10 Aug 2023 02:50:13 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276217bd174625098c340176f9c37306fa340201a5da57b69e268c08d5154d67`  
		Last Modified: Thu, 10 Aug 2023 02:50:34 GMT  
		Size: 198.9 MB (198902134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86c6c002faad2b8d2c2c0a0bbd9f21caca22155b82d3ec5abc1cd22c66c2820`  
		Last Modified: Thu, 10 Aug 2023 02:50:15 GMT  
		Size: 3.8 MB (3839987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a143092aaaf6e7a1400c25de5e11ce0583be13d547b1536b4ff7d614a49edd2b`  
		Last Modified: Thu, 10 Aug 2023 02:50:14 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
