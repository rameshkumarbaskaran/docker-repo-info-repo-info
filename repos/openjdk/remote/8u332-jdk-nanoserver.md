## `openjdk:8u332-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:3530f6e0bd41e84835b0d8d0a6b4e4c15b4db4fa702bf0dd3bcdb886292d6b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `openjdk:8u332-jdk-nanoserver` - windows version 10.0.17763.3165; amd64

```console
$ docker pull openjdk@sha256:3240aa42cbd3cf9db1e2aa5448edc5475a96a6a7190a5b139a12373c75cdf527
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204233352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f576f9d53944b77f0d6f1f883578933bc75c69bbcc2bd1c6616e2bea4c6a7053`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:50:41 GMT
SHELL [cmd /s /c]
# Wed, 13 Jul 2022 16:14:00 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Jul 2022 16:14:01 GMT
USER ContainerAdministrator
# Wed, 13 Jul 2022 16:14:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 Jul 2022 16:14:13 GMT
USER ContainerUser
# Wed, 13 Jul 2022 16:14:13 GMT
ENV JAVA_VERSION=8u332
# Wed, 13 Jul 2022 16:14:29 GMT
COPY dir:679ecdc3b1aa3045788b8b611f7a86f57009d803f478419678a6098b0a258b48 in C:\openjdk-8 
# Wed, 13 Jul 2022 16:14:53 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b09c07c6aeead64423fdefc240fe2e1b6330c96732fd2705113030da84416be`  
		Last Modified: Mon, 18 Jul 2022 21:22:33 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148f24fdace3fb9dfc469abd587650fafdf6306095591fbac5f681ea330560c0`  
		Last Modified: Mon, 18 Jul 2022 21:32:02 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f93316072971a85b9949521e5e6ecf59d21bdc3581fc1e1add713febb868ef0`  
		Last Modified: Mon, 18 Jul 2022 21:32:02 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed149726e806a0166236d15cf4fc5ea65eb1da4033351d46fa58aa3f704aa85`  
		Last Modified: Mon, 18 Jul 2022 21:31:59 GMT  
		Size: 72.7 KB (72654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fcf0621e58eee5b24877bc6f1542450faf983b06d868581b56b39dc69597f3`  
		Last Modified: Mon, 18 Jul 2022 21:31:59 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c95bf4d1ff3d66693e0ce009d29f62edeb2992004e2227a8611a034f690155`  
		Last Modified: Mon, 18 Jul 2022 21:31:59 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ea383cd3094ccb57051abb2896a7ada9969faac3dba8c635ea93ff3ff4535c`  
		Last Modified: Mon, 18 Jul 2022 21:32:12 GMT  
		Size: 100.9 MB (100949441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c974cf81edfb34efbc16685056d1c03458f636f8a6a83706b2617b3cf2d133`  
		Last Modified: Mon, 18 Jul 2022 21:31:59 GMT  
		Size: 50.5 KB (50511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
