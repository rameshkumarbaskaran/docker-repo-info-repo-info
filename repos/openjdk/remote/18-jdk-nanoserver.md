## `openjdk:18-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:5e323522ed769558d927458c31402d04b9b5e5bb5c087401ee1dae4a3c19d0e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `openjdk:18-jdk-nanoserver` - windows version 10.0.17763.2452; amd64

```console
$ docker pull openjdk@sha256:a945b8a048b5fee51dd1edd9e70ce4ad0661f16ca9fd61e8f3d3a326e3d15e94
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.6 MB (290589955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6706f68540eec5b50661a0311336bfad1b0f750eec88a59d2bb1fde55306f5e3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 05:19:56 GMT
SHELL [cmd /s /c]
# Wed, 12 Jan 2022 05:29:01 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 12 Jan 2022 05:29:02 GMT
USER ContainerAdministrator
# Wed, 12 Jan 2022 05:29:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 Jan 2022 05:29:11 GMT
USER ContainerUser
# Wed, 12 Jan 2022 05:29:12 GMT
ENV JAVA_VERSION=18-ea+30
# Wed, 12 Jan 2022 05:29:39 GMT
COPY dir:3d6861a7fa55c63d29eac691cb55df2ed4bfbbb831002267ccd0f83773649293 in C:\openjdk-18 
# Wed, 12 Jan 2022 05:29:54 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 12 Jan 2022 05:29:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:71dcb756adb8534a87210067788d6aa4a5a366b72d022b7af035e5263a3e54a0`  
		Last Modified: Wed, 12 Jan 2022 16:05:17 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35843959f8e0ca6dcfc113050b1cdb5b928728e0a683fb38676c89586a3e2d68`  
		Last Modified: Wed, 12 Jan 2022 23:04:36 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1f2e674c754e5e366b940d467fa78c5384c225c0b9154a421da505279df403`  
		Last Modified: Wed, 12 Jan 2022 23:04:35 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6c5e50381725d68307460bb798ac17ea32e40b81a068c63b7438232aed0d36`  
		Last Modified: Wed, 12 Jan 2022 23:04:35 GMT  
		Size: 74.2 KB (74177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9245449441de27597a990ebf5efd2513b98583d8ca752c0c589cbdf2a083543b`  
		Last Modified: Wed, 12 Jan 2022 23:04:33 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f208d1757245350fc0c28a39128f738e9325e90f5386868fcae34dc7923b3c`  
		Last Modified: Wed, 12 Jan 2022 23:04:33 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6198668ac99fce21c998537b107b082e41bd9ed3f8ee445024e105ac12d217b`  
		Last Modified: Wed, 12 Jan 2022 23:04:53 GMT  
		Size: 184.0 MB (183962485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d129136fb9be1cfee217622d46b304753cfddc3432cc6e29abfc3f3ce81c69`  
		Last Modified: Wed, 12 Jan 2022 23:04:34 GMT  
		Size: 3.5 MB (3515302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd46fa2b587a75f823375d3be0ee1914a41a35714bc951cfda3b48dc4052d26`  
		Last Modified: Wed, 12 Jan 2022 23:04:33 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
