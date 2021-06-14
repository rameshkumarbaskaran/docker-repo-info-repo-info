## `openjdk:17-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:e31828ee0f844123d4e913eaf63e6a41494e138852e649fb7d0c7b33ee803af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `openjdk:17-ea-jdk-nanoserver-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull openjdk@sha256:a7b1020f7fb22bb754b7634743ebc6a8779625ad7cc510bd7f68d469901e90a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288502285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d91c7f98cc184aec644c02c5d6197d7d1572ee6ad6059ba596549b7677466a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 16:52:42 GMT
SHELL [cmd /s /c]
# Wed, 09 Jun 2021 16:52:44 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Jun 2021 16:52:46 GMT
USER ContainerAdministrator
# Wed, 09 Jun 2021 16:53:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Jun 2021 16:53:09 GMT
USER ContainerUser
# Mon, 14 Jun 2021 21:28:57 GMT
ENV JAVA_VERSION=17-ea+26
# Mon, 14 Jun 2021 21:29:16 GMT
COPY dir:c0d0b8fd75c736af391e64c7a28b0f04c37bbd1f02dffb94798a9f345b7e0f5b in C:\openjdk-17 
# Mon, 14 Jun 2021 21:29:41 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 14 Jun 2021 21:29:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e4800203e906d49fbdaf1eeab4de72f28796d5b9a1ea44f8d7461001cfa56614`  
		Size: 102.7 MB (102671454 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:acc28506464ab4d21eaffeb562876f3408463a46d298d12ded7ac0e3dd3c1bd6`  
		Last Modified: Wed, 09 Jun 2021 17:25:28 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a017ad6d2c865b2b606d1d084d50c43233147ea5cf53857802c790c6c01b7c3`  
		Last Modified: Wed, 09 Jun 2021 17:25:26 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c3e213028246803502d07da137fca93406b7b31a282ab02ef95a4e7547b1e1`  
		Last Modified: Wed, 09 Jun 2021 17:25:26 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24145c50d278aaa44ac5a4bc31c1b03bac6fcd0d7e2d291c01685bc9b4260369`  
		Last Modified: Wed, 09 Jun 2021 17:25:26 GMT  
		Size: 69.6 KB (69634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0442665d8729ebbf2ff71dbd067a8b13f6af08edd7d070d9ba24a2e9e30285f8`  
		Last Modified: Wed, 09 Jun 2021 17:25:24 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dedd56f99fe3aa76c0a648d1d209739220b4456c0d2a3bd1867a7f99f4e42be9`  
		Last Modified: Mon, 14 Jun 2021 21:47:10 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b9c8488b85203fb44b55215b41644a504d9e4bb7cec4df8dbdd79a4c45e0f0`  
		Last Modified: Mon, 14 Jun 2021 21:47:30 GMT  
		Size: 182.1 MB (182110229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d2f9651da65ccce8788155f08b5ffbb8716f8d37602a13b44a54ed25e5bcfe`  
		Last Modified: Mon, 14 Jun 2021 21:47:11 GMT  
		Size: 3.6 MB (3644021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e545a377dc799a18bc70f3db04b4d1586a6349e81e1c256dde8d743682809b3`  
		Last Modified: Mon, 14 Jun 2021 21:47:10 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
