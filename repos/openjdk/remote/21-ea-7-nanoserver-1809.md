## `openjdk:21-ea-7-nanoserver-1809`

```console
$ docker pull openjdk@sha256:d9a115da5d41f4fccb7733838a309378f18cee6e0b60e5075b077d3a42c9754d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `openjdk:21-ea-7-nanoserver-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull openjdk@sha256:74e2e213662ddb2458df22dfc2d4afa083881914350e7493bd942c6bf2cc7777
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304634581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18589382c2c308c606069a0d2fe3992ecf8711ff52cd2d9c46d7f8d2e1b32e6`
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
# Mon, 30 Jan 2023 19:19:05 GMT
ENV JAVA_VERSION=21-ea+7
# Mon, 30 Jan 2023 19:19:25 GMT
COPY dir:337582ef715f27a6657a135b1e2c34af138b221c91d5903843788d04871b9b29 in C:\openjdk-21 
# Mon, 30 Jan 2023 19:20:04 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 30 Jan 2023 19:20:05 GMT
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
	-	`sha256:b53b538c5d04d217b22b013b44c45eb12c55ce91ba80445ff2a186340c6a5d47`  
		Last Modified: Mon, 30 Jan 2023 19:28:01 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac03b6f2b66f87dbaebb712802f6f36d8539762c44a8686678daf9df2646d39a`  
		Last Modified: Mon, 30 Jan 2023 19:28:26 GMT  
		Size: 194.1 MB (194096247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb2e13ec52ab4aa7e1a9d2904b7916894594ff80984d76c01a47529bb8e17d6`  
		Last Modified: Mon, 30 Jan 2023 19:28:03 GMT  
		Size: 3.8 MB (3796019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9bb568aea0450bc61e6376c4c8ee99c1c340605f450d554dd39326b97235c6`  
		Last Modified: Mon, 30 Jan 2023 19:28:02 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
