## `eclipse-temurin:8-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:1923625d36801c2a07bd60e4c7a1743aaeb8c6b6ea43a1d9fd80b07ace18f0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.643; amd64
	-	windows version 10.0.17763.2803; amd64

### `eclipse-temurin:8-nanoserver` - windows version 10.0.20348.643; amd64

```console
$ docker pull eclipse-temurin@sha256:45754dac51a33ebfc29538af98b1bee6beddd36c65c3d6bccc24afb6887bcfca
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217842046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a754a9d4bc5719c5c8db76e77e5a932fb0a0e38a1e006872166c65d51fba33e`
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
# Thu, 05 May 2022 18:29:23 GMT
COPY dir:fe4a23cbc3aecb3ea1bcf0dca600117ebc14653b599151b614599054d6b82722 in C:\openjdk-8 
# Thu, 05 May 2022 18:29:37 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:abe961a40d681753e643ba84839636a878aa251d9b21aea9752d2969e6948534`  
		Last Modified: Thu, 05 May 2022 21:26:33 GMT  
		Size: 100.1 MB (100074574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425fe8485bbec7c327c13556fab541cf9e5772e4c9f485296187db662f075c29`  
		Last Modified: Thu, 05 May 2022 21:24:49 GMT  
		Size: 96.3 KB (96268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-nanoserver` - windows version 10.0.17763.2803; amd64

```console
$ docker pull eclipse-temurin@sha256:9a9ba77d771064b5a46c30a4be7e75fc7a80c0887e280cba31f6e8a889d592e4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203334759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3d7deb7dd0a0608f817d1cce54b57fde5cf8a67499ed287debab9208994170`
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
# Thu, 05 May 2022 18:22:18 GMT
COPY dir:fe4a23cbc3aecb3ea1bcf0dca600117ebc14653b599151b614599054d6b82722 in C:\openjdk-8 
# Thu, 05 May 2022 18:22:30 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:45e25e254448277f10da735191a52137837240b8433184b3dd4a981bedf8ba2c`  
		Last Modified: Thu, 05 May 2022 21:21:45 GMT  
		Size: 100.1 MB (100074628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c22ae0e7cff6cd2839c8a12c4439674048c163af7efe529ccd3563ba1f1ec5`  
		Last Modified: Thu, 05 May 2022 21:21:32 GMT  
		Size: 87.0 KB (87025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
