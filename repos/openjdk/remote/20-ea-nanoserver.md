## `openjdk:20-ea-nanoserver`

```console
$ docker pull openjdk@sha256:697128b6c5c6cbec3d4db36253dac5b2fd08ae1f3e8150b0349d8fb5660352a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `openjdk:20-ea-nanoserver` - windows version 10.0.17763.3046; amd64

```console
$ docker pull openjdk@sha256:c10a7191178ec0b4471c4030eb074ef78c76e3177a091d982aa15dfab2c184a6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.0 MB (298967996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f179cc31c69d40e9050fc02a0e7160cbf653ec2ffcd7ba113b8552f2e2b7fa`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jun 2022 19:20:11 GMT
RUN Apply image 10.0.17763.3046
# Wed, 15 Jun 2022 17:30:58 GMT
SHELL [cmd /s /c]
# Thu, 16 Jun 2022 01:19:36 GMT
ENV JAVA_HOME=C:\openjdk-20
# Thu, 16 Jun 2022 01:19:37 GMT
USER ContainerAdministrator
# Thu, 16 Jun 2022 01:19:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 16 Jun 2022 01:19:50 GMT
USER ContainerUser
# Thu, 16 Jun 2022 01:19:51 GMT
ENV JAVA_VERSION=20-ea+1
# Thu, 16 Jun 2022 01:20:08 GMT
COPY dir:b5cbad74990820b409b04bd9fd5aed81bde7dd9b9106b788a5087b8224b547c9 in C:\openjdk-20 
# Thu, 16 Jun 2022 01:20:28 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 16 Jun 2022 01:20:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d555a7e4de4dd775379d5c43c1419374bff7908670dc7444be5e8e8f386f3d26`  
		Size: 103.2 MB (103153235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92b4c385cd5cbb12fb09cb31c12b5e5de38cf7b380c8681286caac242c06d3ed`  
		Last Modified: Wed, 15 Jun 2022 18:22:11 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda95a4aa1ce8b324ff84e1ccdf8befbe50e58a948d31b65618925e2842efada`  
		Last Modified: Thu, 16 Jun 2022 01:33:30 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f66084dce2c5c1fa8b13cd8edb172b48a4411ebf5466035c9c5fef517796cce`  
		Last Modified: Thu, 16 Jun 2022 01:33:30 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273a225993ae008c14a2ad71f55edbcafc99d581fba5b2fd8297a2af9bd6fc2d`  
		Last Modified: Thu, 16 Jun 2022 01:33:30 GMT  
		Size: 71.2 KB (71215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1582199825c588de3fcfbec196a74a70813b8a78abaa2abbed131795de8f1d6`  
		Last Modified: Thu, 16 Jun 2022 01:33:27 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546d93b55a00943d52dc894b20c026feb8fe48016e4ad2bbe4da2244021cab9c`  
		Last Modified: Thu, 16 Jun 2022 01:33:27 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fad7bfe4f93ff45c32baebcb334610efc082d7d68c632cf96195780d0c42331`  
		Last Modified: Thu, 16 Jun 2022 01:36:48 GMT  
		Size: 192.0 MB (192028357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b351b37820b20120ca7697a742608498a49a4d34c4b844dfab3a0a3a4f5952c0`  
		Last Modified: Thu, 16 Jun 2022 01:33:31 GMT  
		Size: 3.7 MB (3708183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7626ffedfec38a8440037e64cbe80096eeaa81d7f282e8ada305beda8a2126e5`  
		Last Modified: Thu, 16 Jun 2022 01:33:27 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
