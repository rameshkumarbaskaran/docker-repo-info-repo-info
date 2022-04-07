## `openjdk:19-ea-16-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:8b948f76dcafc55ce4e83f974b2f79b0d483e3f10bc857639d3c9a323299118a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `openjdk:19-ea-16-jdk-nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull openjdk@sha256:aad28341e0d866b0e90628182665f15803e536ad68ea7b8707311e0a728d7c1c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 MB (294955116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545ac687a7002d179d3be2047fbd43ad4e071be693f4bd65d1a900da11b7ff05`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Tue, 08 Mar 2022 21:56:20 GMT
SHELL [cmd /s /c]
# Wed, 09 Mar 2022 17:13:35 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 09 Mar 2022 17:13:36 GMT
USER ContainerAdministrator
# Wed, 09 Mar 2022 17:13:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Mar 2022 17:13:48 GMT
USER ContainerUser
# Thu, 07 Apr 2022 01:19:53 GMT
ENV JAVA_VERSION=19-ea+16
# Thu, 07 Apr 2022 01:20:08 GMT
COPY dir:3d8dd92ecd62692355dc66702baed53817e6e2c1b89fa385c26830fcf47bf10a in C:\openjdk-19 
# Thu, 07 Apr 2022 01:20:39 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 07 Apr 2022 01:20:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e0065cd23a657c8f30ae5af121fd18451d2307835a1124ea57c80683eda26c94`  
		Last Modified: Tue, 08 Mar 2022 22:37:21 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab71e137ca33aa5127b0e55796dd1ffba9bdcf004bd9e37533e42daa5ebd2bf`  
		Last Modified: Wed, 09 Mar 2022 17:42:19 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b9123b1e06063521bbaeb5ac4dc7ac8960be154774560ca5c9db99a43b2d8d`  
		Last Modified: Wed, 09 Mar 2022 17:42:19 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ab23123853d0353a546935f5a1d10d91f5c5c44d79bf888ae0d353941c6938`  
		Last Modified: Wed, 09 Mar 2022 17:42:19 GMT  
		Size: 68.0 KB (68002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e219e794e6ab490d19f1491c0d2de445c430aac5eceb51f362b916de14e9250d`  
		Last Modified: Wed, 09 Mar 2022 17:42:17 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7faf9940dd708bd8821c65def65e1cbe5d2022800a3c2b3b26757f076bfa3f`  
		Last Modified: Thu, 07 Apr 2022 02:25:15 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937b57461584e1ed727453e99654a07857a4dde3570cdc7a608d17a016e56d9d`  
		Last Modified: Thu, 07 Apr 2022 02:25:33 GMT  
		Size: 188.3 MB (188254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68773a9f7528d71f3ca489ed1679256b8bf1e34249d35c87bcbcc58cf050caf2`  
		Last Modified: Thu, 07 Apr 2022 02:25:16 GMT  
		Size: 3.6 MB (3571120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7c2e1308c40b214cab9b31e73115070ddc232e76c511bcc8297c7697bc829f`  
		Last Modified: Thu, 07 Apr 2022 02:25:15 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
