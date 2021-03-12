## `openjdk:8u282-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:72577d4865b2d103ae2d9e8a71b799151ca34f5ec370ee4d93827ef400d4ff58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `openjdk:8u282-jdk-nanoserver-1809` - windows version 10.0.17763.1817; amd64

```console
$ docker pull openjdk@sha256:80d9f2789173a1624a293bde2223a554a3e75002a0ce1b3f8c36f434adcaffc5
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.5 MB (202545753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d64fcc5c10870ace7a06936ace2536ecab772e53e96f49766a66b6de1bf5239`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 26 Feb 2021 16:47:31 GMT
RUN Apply image 1809-amd64
# Wed, 10 Mar 2021 17:50:47 GMT
SHELL [cmd /s /c]
# Wed, 10 Mar 2021 18:20:23 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Mar 2021 18:20:24 GMT
USER ContainerAdministrator
# Wed, 10 Mar 2021 18:20:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Mar 2021 18:20:39 GMT
USER ContainerUser
# Wed, 10 Mar 2021 18:20:40 GMT
ENV JAVA_VERSION=8u282
# Wed, 10 Mar 2021 18:20:56 GMT
COPY dir:6f6bc9ea1f93ff1db59b5fd63225d3a5b1df7d373dee2c520410df56c408f0e1 in C:\openjdk-8 
# Wed, 10 Mar 2021 18:21:15 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:a11c4ca8f1ba16b6e1395d4523be2215bd0871c2e3e4695b9f2b87bd7472be52`  
		Size: 101.4 MB (101389964 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b1146273d9b624ee892dfcbb3c753523f09f79536a16d63b711cb0027825374a`  
		Last Modified: Wed, 10 Mar 2021 18:33:51 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f11eb2c80ac2b4f762871d1f821267ecf574ea7eddab86391aa5f1625188b40`  
		Last Modified: Wed, 10 Mar 2021 18:53:22 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682ecf1bea150adf507ca265dbeb646a22975ceaaea9ca0b29439ab0984a2295`  
		Last Modified: Wed, 10 Mar 2021 18:53:18 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4cc81123eaefdda98c01ffd98a878a75adebd6b53b17420e85cb8c16d53b89`  
		Last Modified: Wed, 10 Mar 2021 18:53:16 GMT  
		Size: 67.6 KB (67606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001413a768ed2f644d03fbb68da8a4e0a2fb730f93f7011ef044a818791a0b56`  
		Last Modified: Wed, 10 Mar 2021 18:53:16 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213e2efe1aab599ad6c4106598aa49616eb950eff7773712ef9c11c3bcfd6294`  
		Last Modified: Wed, 10 Mar 2021 18:53:15 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dda35878719eef42276b229aa3772eed6b6d71ad0666f385cee661186092f73`  
		Last Modified: Wed, 10 Mar 2021 18:53:30 GMT  
		Size: 101.0 MB (100991511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7505752bb0f356432d19520ec836b242ccc0f5bb4f15072b9c8762767aecbb3f`  
		Last Modified: Wed, 10 Mar 2021 18:53:16 GMT  
		Size: 90.9 KB (90878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
