## `eclipse-temurin:8u302-b08-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:e3deb9534c8f531b6662881f93ecbfbb595697412f32aaf9b0745e0dc7ed6998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `eclipse-temurin:8u302-b08-jre-nanoserver-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull eclipse-temurin@sha256:f8cda11bdfcaa889c9d23c77b3706c038bf868299bd56e55501cadab7a756be2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141890224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48383187f804102d9291e3c7462b4ab9f945aab397144ba38dbe5b7e66b13a2b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Oct 2021 08:01:14 GMT
RUN Apply image 1809-amd64
# Wed, 13 Oct 2021 18:17:55 GMT
SHELL [cmd /s /c]
# Wed, 13 Oct 2021 18:17:55 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Wed, 13 Oct 2021 18:17:56 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Oct 2021 18:17:57 GMT
USER ContainerAdministrator
# Wed, 13 Oct 2021 18:18:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Oct 2021 18:18:12 GMT
USER ContainerUser
# Wed, 13 Oct 2021 18:25:46 GMT
COPY dir:1080d1f1dd1c0d61d0c45958055fb50fcd7599d7396f8e079867cfa7dbefbee8 in C:\openjdk-8 
# Wed, 13 Oct 2021 18:25:59 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:934e212983f208dc2bebc5de38259a6a62f1761868aacfee2cb3585a13b1e24b`  
		Size: 102.7 MB (102661372 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ceff24c3c0c2c360cd3788fcde5c41e1d6601339f4944623c732558a6030e631`  
		Last Modified: Wed, 13 Oct 2021 19:12:58 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a6866648459c8c90f12126f5b6581327f34b272d63e18f40739e16f778fc46`  
		Last Modified: Wed, 13 Oct 2021 19:12:58 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aac33e066c4d2fa8410826e5d04d739d6d41e991236a94b922cf4ebaf15b715`  
		Last Modified: Wed, 13 Oct 2021 19:12:58 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5c294b63503bb6139aede71e930e77fa4e514c8901a63a6c53e016a7dea26d`  
		Last Modified: Wed, 13 Oct 2021 19:12:56 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ce3f1d3adac21aeff64ee5a834658e889931a8e1479364ec54000d7f8d7ddc`  
		Last Modified: Wed, 13 Oct 2021 19:12:56 GMT  
		Size: 67.5 KB (67464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8151227282ea898d559fd7f4485d14af61dfdc7c83babe26baa15f89630d8856`  
		Last Modified: Wed, 13 Oct 2021 19:12:56 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf1a3db4c20f0b571f21486b201d7f8ab6aa14294a41afdbe929746091842f8`  
		Last Modified: Wed, 13 Oct 2021 19:20:34 GMT  
		Size: 39.1 MB (39074957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4685f8c22934f104c438e72dfe121f6aa736ddcb5d1f88d088c5a02af81d4663`  
		Last Modified: Wed, 13 Oct 2021 19:19:50 GMT  
		Size: 81.1 KB (81138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
