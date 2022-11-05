## `eclipse-temurin:8-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:9bd21bce437754765725b86264fa08d21c34d2c216ea563e4c93ce0c4431e6df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `eclipse-temurin:8-nanoserver` - windows version 10.0.20348.1129; amd64

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

### `eclipse-temurin:8-nanoserver` - windows version 10.0.17763.3532; amd64

```console
$ docker pull eclipse-temurin@sha256:fbfcaaccd560adfd1b616bfa657df8bf1698c83ce1ded7713090878d56216950
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207429618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc614dd87126fa6eb372badcd3cfd21338ed70b01b028e7592ef1b227c6b2a08`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Wed, 12 Oct 2022 15:20:49 GMT
SHELL [cmd /s /c]
# Fri, 04 Nov 2022 23:20:52 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:53 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 04 Nov 2022 23:20:54 GMT
USER ContainerAdministrator
# Fri, 04 Nov 2022 23:21:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 04 Nov 2022 23:21:10 GMT
USER ContainerUser
# Fri, 04 Nov 2022 23:21:20 GMT
COPY dir:3f9950b949d84f617218d6370bf5d9344385a96fee23c5d0245f1523c4ce092b in C:\openjdk-8 
# Fri, 04 Nov 2022 23:21:43 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:ce29f4214f0fb0200b149c387d5e94ee47d5705e9bc7b884331390782282065f`  
		Last Modified: Thu, 27 Oct 2022 21:23:38 GMT  
		Size: 106.8 MB (106773776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6a667d76c19fca171390d60fb90c40e16c777050e943a7fe17ad7686841f0f`  
		Last Modified: Wed, 12 Oct 2022 16:02:59 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fabdffb06fee3cd498656c19d16ded4814c2d91955566f2369c053c98d7d09a`  
		Last Modified: Sat, 05 Nov 2022 00:21:51 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe950e7ccacf950f8a6afadf88ba642b61d8f431b750c1c492c34e8e63c83aa`  
		Last Modified: Sat, 05 Nov 2022 00:21:50 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a141dded366014243cb12da390ea19730310db99eeca2bb636f53c39b9d58ef3`  
		Last Modified: Sat, 05 Nov 2022 00:21:48 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94caf7dc7310b16477f5a2e70e6ff6a33e388115180068960531ae36afb6200`  
		Last Modified: Sat, 05 Nov 2022 00:21:49 GMT  
		Size: 70.0 KB (70017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029a208731a2528fee7a97847ccbdc7e6735e5e26ce4cad5d14dc049b53bb185`  
		Last Modified: Sat, 05 Nov 2022 00:21:48 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215b1806b6c1bd106467ffeb146371bdced5baeed6e05c06ed2b4313d4fdd5f1`  
		Last Modified: Sat, 05 Nov 2022 00:22:02 GMT  
		Size: 100.5 MB (100488744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5ff9e37538e46ab0899bc7d2978aff9b1aa533c6b1b210ac5c994bbba8d024`  
		Last Modified: Sat, 05 Nov 2022 00:21:48 GMT  
		Size: 91.3 KB (91281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
