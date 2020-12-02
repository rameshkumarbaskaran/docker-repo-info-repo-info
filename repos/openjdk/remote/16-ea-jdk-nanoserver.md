## `openjdk:16-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:a9d3dc6490c01f55c4c95be0b214d7f89a60353b1e49f03f568d05a896f5abc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `openjdk:16-ea-jdk-nanoserver` - windows version 10.0.17763.1577; amd64

```console
$ docker pull openjdk@sha256:0174e40b829234007ad1a742df4f653d82d5a7e5746927f82cfb593e18382061
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284846032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c7e23554784b08bd956db44618e75dac0306d462e99ebc80c37cf8317b3803`
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
# Tue, 01 Dec 2020 23:19:50 GMT
ENV JAVA_VERSION=16-ea+26
# Tue, 01 Dec 2020 23:20:25 GMT
COPY dir:6336b1ff60809d969311f2212cb803679ca214359f275c6da376ba52e9c4bd75 in C:\openjdk-16 
# Tue, 01 Dec 2020 23:20:53 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Tue, 01 Dec 2020 23:20:53 GMT
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
	-	`sha256:3b8ba3c4293e5a32f9e0a0c2ea1384346dae1a139e277363bb58c6ac98991f77`  
		Last Modified: Tue, 01 Dec 2020 23:26:26 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001d0542482edfce1b58ed3054ae66403fa06090ce60888f076716586d8c181e`  
		Last Modified: Tue, 01 Dec 2020 23:26:52 GMT  
		Size: 179.9 MB (179860312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b90c5f5eefdc419ffc985ea14aa08df7c37913f5121e0c89e3c977aab22152f`  
		Last Modified: Tue, 01 Dec 2020 23:26:27 GMT  
		Size: 3.6 MB (3633472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e237e85aa77fd7de732ccc6fc7e003c839c2365b67a72984e0ebd37eef54c7`  
		Last Modified: Tue, 01 Dec 2020 23:26:25 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
