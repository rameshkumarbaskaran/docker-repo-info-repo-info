## `eclipse-temurin:8u332-b09-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:a1bc986de0811b2383d8274698bdb4bf50ce35ed7b26ee91ce4c3c3f31a2d028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.643; amd64
	-	windows version 10.0.17763.2803; amd64

### `eclipse-temurin:8u332-b09-jre-nanoserver` - windows version 10.0.20348.643; amd64

```console
$ docker pull eclipse-temurin@sha256:42542826183b01df570d6a3a6c10355b386b368661e6085262f960a4258c61e1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156866105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd4b1a87eb5f45f180e8ec7dd813039b617ff89ff9f98b790f031ccbd0be19a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 03 Apr 2022 05:29:07 GMT
RUN Apply image ltsc2022-amd64
# Wed, 13 Apr 2022 15:47:59 GMT
SHELL [cmd /s /c]
# Thu, 05 May 2022 18:29:02 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Thu, 05 May 2022 18:29:03 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 05 May 2022 18:29:04 GMT
USER ContainerAdministrator
# Thu, 05 May 2022 18:29:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 05 May 2022 18:29:12 GMT
USER ContainerUser
# Thu, 05 May 2022 18:29:50 GMT
COPY dir:3ac3da968b0a55dd3b56d678ae78ff2fe7435f143b42a50fa75d097fd864892f in C:\openjdk-8 
# Thu, 05 May 2022 18:30:00 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:5ee98801bdad72bc36678d072c89f7dd482fee29086c1d9c8ad6ff0cb5afa385`  
		Size: 117.6 MB (117579416 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:924a7c42e559a85c0bc74dbb028ddeee43fe67b0f59c81c60cbda0082e0e3ae5`  
		Last Modified: Wed, 13 Apr 2022 16:38:31 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf67650d685fc81e7220c0836b1440badb7ae758b2bd218eec070d83baf9be1`  
		Last Modified: Thu, 05 May 2022 21:24:51 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fba03bb0042bd9768d0055cb3b00be06e2bcd9d3cfc45f5a226242c98830a31`  
		Last Modified: Thu, 05 May 2022 21:24:51 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d11a5f6c9c26ddd2c2850ef9f68e3b3300ad04b2f389bef86300fd6ad7d847`  
		Last Modified: Thu, 05 May 2022 21:24:49 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8726ef9060c764cd7afd8df0bc4f41b128cc870f834ffb81c46cca250e6abb82`  
		Last Modified: Thu, 05 May 2022 21:24:49 GMT  
		Size: 86.2 KB (86162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b486fcf9f8bbb5feb079c1fc12cad15f236a1aba31abe2400950a8eb3125ea`  
		Last Modified: Thu, 05 May 2022 21:24:49 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3412d8a4399f78fdb206e79e74a09f404b5cf19aec19e7d94d311140908a2b1f`  
		Last Modified: Thu, 05 May 2022 21:26:55 GMT  
		Size: 39.1 MB (39133127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2196f390a54b4ba9c1a8acf0fa80585040a72b4fba28ae75255be418ffb0b940`  
		Last Modified: Thu, 05 May 2022 21:26:49 GMT  
		Size: 61.8 KB (61774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u332-b09-jre-nanoserver` - windows version 10.0.17763.2803; amd64

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
