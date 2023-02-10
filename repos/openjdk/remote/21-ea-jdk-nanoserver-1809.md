## `openjdk:21-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:a9e60f39e7f948e5af6ceb0ce1339d4fc47f8936619bd75de9661103e84ab985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `openjdk:21-ea-jdk-nanoserver-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull openjdk@sha256:48a417aade9d3b2157bd8eba89d884e5c6b5bb6f6e7c2d5a2b029b02fec86e7f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.7 MB (304680295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf19eca8f602caac3ccc25b2409c823ccbc1c9a5d47497c7e0de569e20d539f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jan 2023 05:17:01 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:45:31 GMT
SHELL [cmd /s /c]
# Thu, 12 Jan 2023 05:11:18 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 12 Jan 2023 05:11:19 GMT
USER ContainerAdministrator
# Thu, 12 Jan 2023 05:11:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 12 Jan 2023 05:11:35 GMT
USER ContainerUser
# Fri, 10 Feb 2023 02:30:42 GMT
ENV JAVA_VERSION=21-ea+9
# Fri, 10 Feb 2023 02:31:00 GMT
COPY dir:d22ed295da240dffc46c261d95a62ee269aa2940a1a41af4173a504de0e076b2 in C:\openjdk-21 
# Fri, 10 Feb 2023 02:31:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 10 Feb 2023 02:31:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e58f9ad3b15a2a4882ab0a845e8e619cc8c3c411ddbe8b50046c1618a95c1397`  
		Last Modified: Thu, 12 Jan 2023 02:40:44 GMT  
		Size: 106.7 MB (106666138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea67a6bd980bdee35399883e5abcc31c738b338ad384b2f92d91a15cf09d9df`  
		Last Modified: Thu, 12 Jan 2023 02:40:16 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c10d054b2ffa414ee6a75be646bd3ee1ea6bd5a11e2400c757afeb68d8c6d4`  
		Last Modified: Thu, 12 Jan 2023 05:23:44 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e99b18c6e5f683aa5e6fa7ad7ce124fabae3b048287a183a71a7dc15df8ef6a`  
		Last Modified: Thu, 12 Jan 2023 05:23:44 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6700bb1c6480ee456d21843fdd01e9a05b05ea2d8ac6f54cbd75acbaafe6ab52`  
		Last Modified: Thu, 12 Jan 2023 05:23:44 GMT  
		Size: 69.3 KB (69271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fc3250a046295f3386717ccc0548a5954c2c32fb3c4bbbc83dc8fdd13e1c27`  
		Last Modified: Thu, 12 Jan 2023 05:23:42 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2d3a1f742fb5d49411322ec0445ddb2cb9d5414c8d187bf84dce3205d4f040`  
		Last Modified: Fri, 10 Feb 2023 08:20:48 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2805802b0a1c857779ba4314692f4224d81591dad07e729b870982e4b4c4355c`  
		Last Modified: Fri, 10 Feb 2023 08:21:15 GMT  
		Size: 194.1 MB (194141513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c398986d50926eb3490130338502c6afb5427393f9fd5a5799d341e15de387`  
		Last Modified: Fri, 10 Feb 2023 08:20:49 GMT  
		Size: 3.8 MB (3796498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c035415dbc675eae1eb82a796da111d619c4e393bb97898222169ec1a0dbaf3d`  
		Last Modified: Fri, 10 Feb 2023 08:20:48 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
