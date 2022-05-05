## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:90d62c5839ccae14f84a07a0cd035073d1e8257944591a27f36e88a3b70f8643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull eclipse-temurin@sha256:2419dda41341f7568d5c96639ed93a346997c33a49b2142921c087b94e5643c8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142353211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764b3e3530c95eeeb9135238385c946064f49d8778eed9c3f4595771fef60af7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 15:16:11 GMT
SHELL [cmd /s /c]
# Thu, 05 May 2022 18:21:57 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Thu, 05 May 2022 18:21:58 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 05 May 2022 18:21:59 GMT
USER ContainerAdministrator
# Thu, 05 May 2022 18:22:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 05 May 2022 18:22:07 GMT
USER ContainerUser
# Thu, 05 May 2022 18:26:39 GMT
COPY dir:3ac3da968b0a55dd3b56d678ae78ff2fe7435f143b42a50fa75d097fd864892f in C:\openjdk-8 
# Thu, 05 May 2022 18:26:48 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ea4009814dceb50337c66614a6008cfc2fb73ce53e62162bce071ef6ea1adf2d`  
		Last Modified: Wed, 13 Apr 2022 15:58:06 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83afa91e4aec5329bd70d182ed3cffd364b9a3bc05dacfc0fffeff45fa4f91c`  
		Last Modified: Thu, 05 May 2022 21:21:34 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e54e2aa3af614ff21384527d270fdf1ee2edef1927fb30fc0e8985df2fa4c20`  
		Last Modified: Thu, 05 May 2022 21:21:35 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b54b9b531a5bfdf940bda84913224267dd3e96cbb7ef8f1629a22c7be9f3995`  
		Last Modified: Thu, 05 May 2022 21:21:32 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633af794b63d5974857cb963d376a9ac1040ec2a723f821dec95c92950551a83`  
		Last Modified: Thu, 05 May 2022 21:21:32 GMT  
		Size: 71.3 KB (71278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e682d44e483a1b8f0c7ae2496bda2fbb6395276992767071b780e4549501b0ac`  
		Last Modified: Thu, 05 May 2022 21:21:32 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bf3415cb27c3c31cb8bf452789f17009f59c477bdfd9b4cf084bd10088d396`  
		Last Modified: Thu, 05 May 2022 21:24:25 GMT  
		Size: 39.1 MB (39129112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5dbc232e159060a02de51efc3a73182e5665bd14aecba4da4fe5db14d5228c4`  
		Last Modified: Thu, 05 May 2022 21:23:44 GMT  
		Size: 51.0 KB (50993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
