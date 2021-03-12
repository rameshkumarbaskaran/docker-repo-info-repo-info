## `openjdk:8u282-jre-nanoserver`

```console
$ docker pull openjdk@sha256:dee9f817bb076ea02e5240ea27b9de55e3b4d81291e34f51cfb87621e8e6067d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `openjdk:8u282-jre-nanoserver` - windows version 10.0.17763.1817; amd64

```console
$ docker pull openjdk@sha256:121c755d38367f847f4f601f9b56b89e20a1c23eea75ac0002644d30c91af06d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139744569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1c40f2f505bd7cc734fe94f0f4bc8fb9c127b7f3b7ac710108e6d809de020c`
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
# Wed, 10 Mar 2021 18:24:21 GMT
COPY dir:f51b6315789fea62bc81073100310d85cf4082234fc7f3bd9b51f6f4a883a8f3 in C:\openjdk-8 
# Wed, 10 Mar 2021 18:24:37 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version 	&& echo Complete.
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
	-	`sha256:6165544a7ad91a6146f21725b9a00a2bd0a0ecfea523ea4f6d973261b515e4dd`  
		Last Modified: Wed, 10 Mar 2021 18:54:45 GMT  
		Size: 38.2 MB (38198958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7eba2ff92f0b8b88c3caaa1d17f5af53e99b54d562ce97b284c1682318ba2c`  
		Last Modified: Wed, 10 Mar 2021 18:54:34 GMT  
		Size: 82.2 KB (82247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
