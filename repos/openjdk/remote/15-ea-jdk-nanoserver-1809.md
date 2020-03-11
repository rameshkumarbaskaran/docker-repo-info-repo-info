## `openjdk:15-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:0ad9a36893c0bfa601424a258a715a0fc94922010bd441d47fd12c2cd191f9c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `openjdk:15-ea-jdk-nanoserver-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull openjdk@sha256:8831683685b01a57a2a6584313a4a7a3075316aa4ad376fbd5dbddcbfe0d6406
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297867253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e03ee3d553feccf235084d902e805bc716027241e08abcaeafd7dc7e1a81b0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:56:25 GMT
SHELL [cmd /s /c]
# Wed, 11 Mar 2020 14:56:27 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 11 Mar 2020 14:56:28 GMT
USER ContainerAdministrator
# Wed, 11 Mar 2020 14:56:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 11 Mar 2020 14:56:55 GMT
USER ContainerUser
# Wed, 11 Mar 2020 14:56:56 GMT
ENV JAVA_VERSION=15-ea+13
# Wed, 11 Mar 2020 14:57:54 GMT
COPY dir:381680c6d29a098adbd773948a72f80f540fcd0de924f6456602295be249872c in C:\openjdk-15 
# Wed, 11 Mar 2020 14:58:13 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Wed, 11 Mar 2020 14:58:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4a66be005a5120fc8bbc31290c77aa0e6580d02bc61948ef0602bf09a6ab61ba`  
		Last Modified: Wed, 11 Mar 2020 15:26:11 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa222a675c58ae4e16af815d117d614899889b99615416d258fea25600f704cc`  
		Last Modified: Wed, 11 Mar 2020 15:26:08 GMT  
		Size: 931.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca058e8ce192a6fd627d0c85ec3d6b2843d8adc7b0a24db65d4460a1388d514`  
		Last Modified: Wed, 11 Mar 2020 15:26:08 GMT  
		Size: 934.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9adfe4646dd92a1ea69c4f00cecd622a93c1467830cd992635a0ba3bc689db93`  
		Last Modified: Wed, 11 Mar 2020 15:26:08 GMT  
		Size: 67.2 KB (67155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5348a60ea8643e6600613c06514ce34cb7bf596bd992df4b5f09a9e3b9226f76`  
		Last Modified: Wed, 11 Mar 2020 15:26:04 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23ce5a15d61cb174c6503738905e9b2bcfbbb645008f3886107511a6953f16`  
		Last Modified: Wed, 11 Mar 2020 15:26:04 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f2ab640e4721af49cdec6cb367b52751fe105a2408c606dcacc8bc27e678bd`  
		Last Modified: Wed, 11 Mar 2020 15:26:40 GMT  
		Size: 193.3 MB (193313877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607f4e851df0c2e1363e837e874b227d6a2c3455212ea300aea2721cfd6b0b55`  
		Last Modified: Wed, 11 Mar 2020 15:26:06 GMT  
		Size: 3.4 MB (3430333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d70d7439c0722f1d02fc353e011e7d7eddea1cf3ed71148dff31b3936e40a53`  
		Last Modified: Wed, 11 Mar 2020 15:26:04 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
