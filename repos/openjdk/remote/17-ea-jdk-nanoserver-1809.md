## `openjdk:17-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:67c1060ed5ff2d2bf5b14d327e534131bb312d46fd28721ce21032a250330a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1935; amd64

### `openjdk:17-ea-jdk-nanoserver-1809` - windows version 10.0.17763.1935; amd64

```console
$ docker pull openjdk@sha256:1bb502dbd8f68af429c27e225c8ff4cb8402b293a1e6e2bd82d310f5e4e69d29
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286079872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e180403bfd965495fcc7bdd15937597bec10cdc33536eb62b3d2b39e2ec3be`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 May 2021 11:54:57 GMT
RUN Apply image 1809-amd64
# Wed, 12 May 2021 16:42:56 GMT
SHELL [cmd /s /c]
# Wed, 12 May 2021 16:42:56 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 May 2021 16:42:57 GMT
USER ContainerAdministrator
# Wed, 12 May 2021 16:43:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 May 2021 16:43:21 GMT
USER ContainerUser
# Fri, 04 Jun 2021 20:39:01 GMT
ENV JAVA_VERSION=17-ea+25
# Fri, 04 Jun 2021 20:39:22 GMT
COPY dir:2cba33c1c102797dc756ff46d5def95468416517112f1eba2a9b024090e94db0 in C:\openjdk-17 
# Fri, 04 Jun 2021 20:39:56 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 04 Jun 2021 20:39:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b9043d31610e0dfa43b1afe286f8918b6e3bf69ece50f44424b29d48f20aa662`  
		Size: 101.4 MB (101375240 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ea91a7775c05d55a850a2983043468ce6ded7406743836cf8f33afb037aba1a8`  
		Last Modified: Wed, 12 May 2021 17:16:41 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec0a5b4dd190af3527c02bb783babc5d88014a4de37555355c2f7a59dd21449`  
		Last Modified: Wed, 12 May 2021 17:16:40 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aab5fc14de7c93823ea1579b64e1e79017e9738a39e5d165aeed23c15bf7ffd`  
		Last Modified: Wed, 12 May 2021 17:16:40 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1954cb2ae96dfb0f537ce02738b91077c41cda7743ff097b99d8a6cfc74e211f`  
		Last Modified: Wed, 12 May 2021 17:16:40 GMT  
		Size: 69.5 KB (69533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95581d66523cc5b44afdfbd1f1e7732689ad5d73bf1c1352ef8f1e669dceede2`  
		Last Modified: Wed, 12 May 2021 17:16:37 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f379f9f84725d283d3d32c44f11b6fbc2cd49b5d03d89e0fde0127a85060d334`  
		Last Modified: Fri, 04 Jun 2021 20:45:33 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa0eb1e63ba43684140bc3631aec71b0f4cf310d1cc4475b0ec946ed604b33c`  
		Last Modified: Fri, 04 Jun 2021 20:49:04 GMT  
		Size: 181.0 MB (180988629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc7bbcc676aa24e311abb1f6b647fe14164c12c6a1dd50f4b20242f6ba9ae27`  
		Last Modified: Fri, 04 Jun 2021 20:45:34 GMT  
		Size: 3.6 MB (3639623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6febf334c3a4ac5a63c353b889618f52d731b950be038d0326617a99c9f232da`  
		Last Modified: Fri, 04 Jun 2021 20:45:33 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
