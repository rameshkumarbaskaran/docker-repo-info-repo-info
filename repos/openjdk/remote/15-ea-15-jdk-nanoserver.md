## `openjdk:15-ea-15-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:728c4d42ceed6f402c165877d5a88284f8a0747a3dedfec5a3db4c8995b66b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `openjdk:15-ea-15-jdk-nanoserver` - windows version 10.0.17763.1098; amd64

```console
$ docker pull openjdk@sha256:6c2578b76531354f57f870bbdf5918f73332f9ba5229f6a0a723ea7191f1e893
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297848533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd41339b6b97ec94560ada5b8a6e448e08877f598c2ff76ac244154065e4c5f`
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
# Mon, 23 Mar 2020 21:19:57 GMT
ENV JAVA_VERSION=15-ea+15
# Mon, 23 Mar 2020 21:20:42 GMT
COPY dir:159c7c7c5fbb6332e8f3f5e4662c731df376737b3ee0f674edeb3f0cc6369b07 in C:\openjdk-15 
# Mon, 23 Mar 2020 21:21:07 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Mon, 23 Mar 2020 21:21:08 GMT
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
	-	`sha256:e4da3230bc3268f2cf8e70381e83f6a559eb5ea1312717c8d5df5634a3985f0e`  
		Last Modified: Mon, 23 Mar 2020 21:28:57 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199a3f2c2702f92d7d072bd115b29550b83f8c06e4bb672cf031b9057daa4d6e`  
		Last Modified: Mon, 23 Mar 2020 21:29:18 GMT  
		Size: 193.3 MB (193290750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806598b45cd2541ae60b9790d705877fa2231d909a7b387ab1be0d8ab19b4a6c`  
		Last Modified: Mon, 23 Mar 2020 21:28:59 GMT  
		Size: 3.4 MB (3434876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524c15903edb41c42e516cd6c5d0823114f7e1443071e83c63129b3022537704`  
		Last Modified: Mon, 23 Mar 2020 21:28:57 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
