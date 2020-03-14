## `openjdk:15-nanoserver`

```console
$ docker pull openjdk@sha256:f5ab47d361b01362654d647c0ad275d41465cae3b37274f3036a6eaf8aec11ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `openjdk:15-nanoserver` - windows version 10.0.17763.1098; amd64

```console
$ docker pull openjdk@sha256:44e9ffc72ad43fcb5e231634f4487f31b641abc55d6f8d19ab68d25066f4e453
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297855117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738c97f16f2bae140bbca4fb6b35967c903279f307386d57d3bf649a9461ea4a`
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
# Fri, 13 Mar 2020 21:39:02 GMT
ENV JAVA_VERSION=15-ea+14
# Fri, 13 Mar 2020 21:39:53 GMT
COPY dir:58ee7b7f635c20386bd237359d36c125ece1d16fa38ddf08305eb51ec9562b54 in C:\openjdk-15 
# Fri, 13 Mar 2020 21:40:17 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 13 Mar 2020 21:40:18 GMT
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
	-	`sha256:0e43b757ddd0dfb986b28c89b210e80c346a422fb338b1f129662261ee066a46`  
		Last Modified: Fri, 13 Mar 2020 22:10:48 GMT  
		Size: 962.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ba499e85b4d74f09ab62bb686c133d8aaf0a540273594c19c8b81a904cfc4a`  
		Last Modified: Fri, 13 Mar 2020 22:11:11 GMT  
		Size: 193.3 MB (193300820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a29d89a409711a72a78abc423c16ad5a510695fb03b147107590766d8afa8f`  
		Last Modified: Fri, 13 Mar 2020 22:10:49 GMT  
		Size: 3.4 MB (3431252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e276c796d15c86513dabe550ab91984af74d3ca8bd4c3c7ae7ef55bb613213c8`  
		Last Modified: Fri, 13 Mar 2020 22:10:48 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
