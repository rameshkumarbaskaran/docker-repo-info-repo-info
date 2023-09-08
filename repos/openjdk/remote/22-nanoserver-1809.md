## `openjdk:22-nanoserver-1809`

```console
$ docker pull openjdk@sha256:dde6701e84accc20ace6e7b0732ba78f087b18518304f93d88c65852b2947d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `openjdk:22-nanoserver-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull openjdk@sha256:ae220c2b228d0795049e615ac106e261fb9d239c47c1530cdf111e0133135fc3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307354586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef690e67771bc741c429076aebf3b35f90e068ec209ff02adb1d9ca1d344b4b`
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
# Fri, 08 Sep 2023 19:37:16 GMT
ENV JAVA_VERSION=22-ea+14
# Fri, 08 Sep 2023 19:37:31 GMT
COPY dir:3e93a63762464c4297fd9a428ab7cbf0f98d649f815f43061cc035465db3383d in C:\openjdk-22 
# Fri, 08 Sep 2023 19:37:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 08 Sep 2023 19:37:44 GMT
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
	-	`sha256:233f991b1c284f1ac7211879b539400ccb2cbc3ca1ceae38c9aadaeb7c657028`  
		Last Modified: Fri, 08 Sep 2023 19:40:24 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a09b57ff649b189d62f446a32e2dbe2cb96f3e0ca5d49ca4e3cd32e98907ed`  
		Last Modified: Fri, 08 Sep 2023 19:40:45 GMT  
		Size: 199.0 MB (198983175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac435abe8f267a1de795e4ae29257af10cd07b5325f2503d46f22bf9b7fa426`  
		Last Modified: Fri, 08 Sep 2023 19:40:25 GMT  
		Size: 3.8 MB (3834027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c48fc557e1d3593832a4ef55fd01b924f175542701239cff7d5766bd27e3d35`  
		Last Modified: Fri, 08 Sep 2023 19:40:24 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
