## `openjdk:20-ea-nanoserver`

```console
$ docker pull openjdk@sha256:51645bcd4fe4baf51e992bffaba0175cbed334676cc03dcce3cef676205bb142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `openjdk:20-ea-nanoserver` - windows version 10.0.17763.3770; amd64

```console
$ docker pull openjdk@sha256:d753b89ed75c26addcd22edc3ce1ae0ea3337f9d40e82458c5971774fffbb0f6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303573094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821b3ccf5522339d3cf7005ddbc963b998e9d0947287a39ee4ede64c53c5c423`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Tue, 13 Dec 2022 22:53:34 GMT
SHELL [cmd /s /c]
# Wed, 14 Dec 2022 03:06:29 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 14 Dec 2022 03:06:30 GMT
USER ContainerAdministrator
# Wed, 14 Dec 2022 03:06:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Dec 2022 03:06:50 GMT
USER ContainerUser
# Fri, 06 Jan 2023 19:30:29 GMT
ENV JAVA_VERSION=20-ea+30
# Fri, 06 Jan 2023 19:30:52 GMT
COPY dir:aec8fae8b96ffb958379616da8ed90a3be329e47c17a2705b14c710fc0ab1c3a in C:\openjdk-20 
# Fri, 06 Jan 2023 19:31:40 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 06 Jan 2023 19:31:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fe06cbef5ac46e54edd743daf1bc2bfa36b294c7ce9104837061c41a4bde7b`  
		Last Modified: Tue, 13 Dec 2022 23:57:01 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8407ccbdbd1b98118842fe985781ff7ccce1a4a02763ce3c7bc5182f0a6cd7be`  
		Last Modified: Wed, 14 Dec 2022 08:49:25 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10a11487b55c583a71e65de52b66756da77520bd91e60c286f53bc275c4776e`  
		Last Modified: Wed, 14 Dec 2022 08:49:25 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b8c7b08a7b6bda536e75dce577a2de479c5b5ac157ae753b5d69a3246b69fc`  
		Last Modified: Wed, 14 Dec 2022 08:49:25 GMT  
		Size: 65.0 KB (65047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4410bf6b8361419a87afad95e1191ea2013d36ec41631d7c8a157b17687c9da4`  
		Last Modified: Wed, 14 Dec 2022 08:49:23 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27979f6ad40fa654440d37af253848ab0f6e57e988fad1248e9f5500841d862`  
		Last Modified: Fri, 06 Jan 2023 20:21:59 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5e4c03ff70d1c09c306691f4d237a30a11ca301d1bb691c6efd436e25e3864`  
		Last Modified: Fri, 06 Jan 2023 20:22:21 GMT  
		Size: 193.1 MB (193056864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b15ebf58fcf3cae646ef1ef7b4919a84c76bb8c2d7a9b1fb508eb0604c3607b`  
		Last Modified: Fri, 06 Jan 2023 20:21:59 GMT  
		Size: 3.8 MB (3773273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb89e3ebbd8088c17da35bb89fec3bda407d88ce380a430038092dab03a97346`  
		Last Modified: Fri, 06 Jan 2023 20:21:58 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
