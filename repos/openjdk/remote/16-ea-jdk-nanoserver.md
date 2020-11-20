## `openjdk:16-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:f7163e955a31f40643fe75c8846f33d9f274d51dcf703e32dfba5b30a98051c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `openjdk:16-ea-jdk-nanoserver` - windows version 10.0.17763.1577; amd64

```console
$ docker pull openjdk@sha256:f17d59983871412be3f10e8120e2ae97a41be4a89b7143d0e6f08ff976971f8f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.2 MB (284153817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733a0514d57e0a3cd115eb396937831ce9d0922b584212b3d3fcfca3873c070e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:53:16 GMT
SHELL [cmd /s /c]
# Wed, 11 Nov 2020 17:53:16 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 11 Nov 2020 17:53:17 GMT
USER ContainerAdministrator
# Wed, 11 Nov 2020 17:53:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 11 Nov 2020 17:53:32 GMT
USER ContainerUser
# Fri, 20 Nov 2020 00:19:54 GMT
ENV JAVA_VERSION=16-ea+25
# Fri, 20 Nov 2020 00:20:29 GMT
COPY dir:add6235a3907b33255cb1edc57b0448235deb83e40dff6740c71f20bc43ea3b0 in C:\openjdk-16 
# Fri, 20 Nov 2020 00:20:55 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 20 Nov 2020 00:20:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:41b7be9dc08821cf81d29b16e0df54f7f3e3aeaa6407f43520c6259f2d84b10c`  
		Last Modified: Wed, 11 Nov 2020 18:27:27 GMT  
		Size: 864.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e637122599038842d743045a8ebfbfa35dbadf7dfee0adcc2ba903e891ab072d`  
		Last Modified: Wed, 11 Nov 2020 18:27:25 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7fa5c85bf3c3dc79cf3bec9aba597aa0b5c38c234952da905e86d7a556b6f3`  
		Last Modified: Wed, 11 Nov 2020 18:27:25 GMT  
		Size: 912.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9c6b451f516c5e78ab16ded450d01a2a45dd13d0cac12cb9b043f5d87f993a`  
		Last Modified: Wed, 11 Nov 2020 18:27:25 GMT  
		Size: 67.3 KB (67302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac0f27f5ace77a66a18d26e72bf8f24216110f8ed5b6f951597b9a42d3ae52b`  
		Last Modified: Wed, 11 Nov 2020 18:27:22 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9499eb88223fc5d71f26606035d2f540520baa78df1b433818a68199c1c991f1`  
		Last Modified: Fri, 20 Nov 2020 00:29:32 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb2bf820d162d2f21dc93a831916c27bf8738cd80392debd8a2fafa321b0b23`  
		Last Modified: Fri, 20 Nov 2020 00:29:51 GMT  
		Size: 179.2 MB (179173548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8826cfb9413f7b925efa4957a7f01c9193c2489062fca5b5695adf3ebfab9d23`  
		Last Modified: Fri, 20 Nov 2020 00:29:34 GMT  
		Size: 3.6 MB (3628017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4b29a34958187d5f6a116a9db851544eeeb59259475fc25cfbf12ec230ca61`  
		Last Modified: Fri, 20 Nov 2020 00:29:33 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
