## `eclipse-temurin:8-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:72b4b9aca2ef2ddca1ee5f5044673200336fe30e245775e135a5572c281626d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `eclipse-temurin:8-nanoserver-1809` - windows version 10.0.17763.2803; amd64

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
