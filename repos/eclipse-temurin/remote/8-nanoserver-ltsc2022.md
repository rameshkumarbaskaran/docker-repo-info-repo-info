## `eclipse-temurin:8-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:7b32e1abb9834ead402a10e2acd5cc99f6d425581d62730b8e47be111f2c19f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `eclipse-temurin:8-nanoserver-ltsc2022` - windows version 10.0.20348.1129; amd64

```console
$ docker pull eclipse-temurin@sha256:5800f114d6fbb4efdc3224fc9cf02390f9223a9673cf6f326caa7c9da47f78ef
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.7 MB (222659247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2068c47d8157d6573769b87743d14d4b35a64e982b80dd6b794dad41ae3307`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Oct 2022 21:37:41 GMT
RUN Apply image 10.0.20348.1129
# Wed, 12 Oct 2022 15:54:21 GMT
SHELL [cmd /s /c]
# Fri, 04 Nov 2022 23:39:15 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:39:16 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 04 Nov 2022 23:39:17 GMT
USER ContainerAdministrator
# Fri, 04 Nov 2022 23:39:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 04 Nov 2022 23:39:38 GMT
USER ContainerUser
# Fri, 04 Nov 2022 23:39:49 GMT
COPY dir:3f9950b949d84f617218d6370bf5d9344385a96fee23c5d0245f1523c4ce092b in C:\openjdk-8 
# Fri, 04 Nov 2022 23:40:13 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:b6520318982addabaf67d0cef5499282d15348f205cf5d7328925bcd681e85bd`  
		Last Modified: Tue, 25 Oct 2022 22:04:15 GMT  
		Size: 122.0 MB (122003513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ed0041e3584df1952980c3f73fd2b6e154328c7a0165f37dbe92ef94ae8a95`  
		Last Modified: Wed, 12 Oct 2022 16:12:53 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95809cf8ef923c767b7953d30af5ca933179ebe310f41272c94409628ab7317`  
		Last Modified: Sat, 05 Nov 2022 00:26:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb651dc877e82864217b0cc3ce7819ed73fe3099aae266fde4d8371b8fc61766`  
		Last Modified: Sat, 05 Nov 2022 00:26:51 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d82c60c747cd53aa1eba03c2c4a811bea3ce486fa34e6fff7133b6db31383d`  
		Last Modified: Sat, 05 Nov 2022 00:26:49 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9db15f529310d0afff94586feed5c2e8342060c276755e3f12324acd35f5b7b`  
		Last Modified: Sat, 05 Nov 2022 00:26:49 GMT  
		Size: 85.2 KB (85211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d3c46d9d9cd54570a0d0df563ff06fc76ffb006db566305ff75b5099c3b4fd`  
		Last Modified: Sat, 05 Nov 2022 00:26:49 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a177dc6120f0eebdd30b336dc44c2d97bd998360466515b07c173a6538276f76`  
		Last Modified: Sat, 05 Nov 2022 00:27:02 GMT  
		Size: 100.5 MB (100502930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebf10de8d38871e8b6bbdb96dc5463b306796d282f318738889ea4d13089512`  
		Last Modified: Sat, 05 Nov 2022 00:26:49 GMT  
		Size: 61.9 KB (61881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
