## `eclipse-temurin:17-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:6fe28cb9db08698a9d87835325c57cd5dd70e7c394038d8dd8dea5f213ad7008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `eclipse-temurin:17-jdk-nanoserver-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull eclipse-temurin@sha256:60ed751e7ad12802a360d68c7cbdfc9a9a2d19a6586dfd54525003f35a064fa7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291847424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7537068e915174822988c372202a383cf1e92f8d827be95731383ad4daa74c18`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:45:32 GMT
SHELL [cmd /s /c]
# Wed, 09 Feb 2022 20:14:27 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Wed, 09 Feb 2022 20:14:28 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Feb 2022 20:14:28 GMT
USER ContainerAdministrator
# Wed, 09 Feb 2022 20:14:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Feb 2022 20:14:38 GMT
USER ContainerUser
# Wed, 09 Feb 2022 20:15:10 GMT
COPY dir:af72ba1102e9cda7f5ea9974b0cafbe96b2f97690adb0743202a1c732a987a84 in C:\openjdk-17 
# Wed, 09 Feb 2022 20:15:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Feb 2022 20:15:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5a7f567e84a5a148036156650a47ef7eec0187f17e880d3b475e51dacd70077b`  
		Last Modified: Wed, 09 Feb 2022 19:20:50 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff9a6949b337ee2cf8190807249bcc9fa8f67cfd1d72a4371750bf483cde6ce`  
		Last Modified: Thu, 10 Feb 2022 21:12:53 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a85abfd5586f64024d88a765fd0921366b7b31d57f0dccf45f0607844c1f8e5`  
		Last Modified: Thu, 10 Feb 2022 21:12:53 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ddbe55c6acad01f3f736dd4e0a2f376883cb43b47086f1440abb55839fb1c6`  
		Last Modified: Thu, 10 Feb 2022 21:12:53 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a0583e34d0ca468f6787b83d5f06f152331457e865656536ca50644678e191`  
		Last Modified: Thu, 10 Feb 2022 21:12:50 GMT  
		Size: 70.2 KB (70234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5dbb6c04a70d0d5eb61cda171231a7dd89010832f12bfe06ad89e81be06eae4`  
		Last Modified: Thu, 10 Feb 2022 21:12:50 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0822f4677d5f9cf33adcd3a61108babcc090914d97fa6790ffa1e691aeadd67`  
		Last Modified: Thu, 10 Feb 2022 21:13:10 GMT  
		Size: 185.0 MB (185022646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9641508d42a6510abcdda279dd95ff8e38803ff4ec84961e9e7c503ba93bc90`  
		Last Modified: Thu, 10 Feb 2022 21:12:54 GMT  
		Size: 3.7 MB (3660487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c2fa7e960f7cb56d9a0ce8c71f9ae8dffece4729ac08b32449d3f4e3dd3248`  
		Last Modified: Thu, 10 Feb 2022 21:12:50 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
