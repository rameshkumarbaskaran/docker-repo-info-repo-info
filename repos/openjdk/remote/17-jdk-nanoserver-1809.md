## `openjdk:17-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:9d43c8bc2e5eb0414426c3ab059b54fab51b27bdc0f344d2bc48fa27add8c345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:17-jdk-nanoserver-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:421ab91ecdb5af231774bc6176f0e89baaedea06233e851702f7db6bd6f71da8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286308230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bcda7924c8d85c5ef8701b760e96a574eb4939887a1d87dde50645c3f23c7f4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:56:48 GMT
SHELL [cmd /s /c]
# Wed, 13 Jan 2021 19:56:48 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 13 Jan 2021 19:56:49 GMT
USER ContainerAdministrator
# Wed, 13 Jan 2021 19:57:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 13 Jan 2021 19:57:07 GMT
USER ContainerUser
# Fri, 15 Jan 2021 23:21:28 GMT
ENV JAVA_VERSION=17-ea+5
# Fri, 15 Jan 2021 23:21:52 GMT
COPY dir:2e19eacdc5f4886729b6967a4101a2cba30a2f1d4ea035d66466237e62585c01 in C:\openjdk-17 
# Fri, 15 Jan 2021 23:22:32 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 15 Jan 2021 23:22:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c2b6c001c337f812bceb3b03d15a70d1d9905540658e751e42f20f7cc0ddc819`  
		Last Modified: Wed, 13 Jan 2021 21:16:47 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788a0bd344d2eb3850ddd4570305cbcf959de9a743a310f941c297081c240d8f`  
		Last Modified: Wed, 13 Jan 2021 21:16:46 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db311194c9cbd0c67151ee177949a18a7ad83e5551b659b30ef3151062c5a98`  
		Last Modified: Wed, 13 Jan 2021 21:16:47 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a588d5e7e84f7b20f460bb66a5bb1f2b7e762713923669ac453e6eda8b23eb7`  
		Last Modified: Wed, 13 Jan 2021 21:16:44 GMT  
		Size: 68.0 KB (68013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df625a811b1b58029fb5e4c987218865063cb248bd9d163cc15c8584c8af7afd`  
		Last Modified: Wed, 13 Jan 2021 21:16:40 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d38b9503e91864f944e9d5878caab9bd9348b0ecccd83771ae8774099a870f6`  
		Last Modified: Fri, 15 Jan 2021 23:36:28 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ee270b6f2fb5902e4d3c4bed643ee4a456dd2e693fe40f02afbd0b59a5fc03`  
		Last Modified: Fri, 15 Jan 2021 23:36:49 GMT  
		Size: 181.2 MB (181213580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd290e0ea8ce4d2b387356dcd00155b37466fc0a77d3d0abcad4031f41ddfb5`  
		Last Modified: Fri, 15 Jan 2021 23:36:30 GMT  
		Size: 3.7 MB (3680880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b17177570e3547e8b0b923affb9c17cbde324b3e51a2ae23269d2a030e41ff0`  
		Last Modified: Fri, 15 Jan 2021 23:36:29 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
