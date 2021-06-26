## `openjdk:17-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:6a3f42ce01f2c649584b08aeda028b4486a51640867cbac9a59b017ce91d5a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `openjdk:17-jdk-nanoserver-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull openjdk@sha256:a95d9516ef985c25f2917154f2ac455fd2fd5fa93f985137e72e18eb6f7f6d10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288459586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dffeeb20d6fcff9d5cf752fede088d8e7f0940c3f1a9067d2d39e9096867e4`
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
# Sat, 26 Jun 2021 01:34:01 GMT
ENV JAVA_VERSION=17-ea+28
# Sat, 26 Jun 2021 01:34:19 GMT
COPY dir:e75f71166cc838d8d369dfe57e40f75376249c947443ccde99a32e96550951ca in C:\openjdk-17 
# Sat, 26 Jun 2021 01:34:52 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 26 Jun 2021 01:34:55 GMT
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
	-	`sha256:25d5ac23bf4e5e3d508ef2aa1a0f40660e1614b5eb21815393ca0ddb22923c1c`  
		Last Modified: Sat, 26 Jun 2021 01:43:05 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c05f66a4f793980f73f76d590496e71f53585f507608b5f90aa04c310d03707`  
		Last Modified: Sat, 26 Jun 2021 01:46:37 GMT  
		Size: 182.1 MB (182067039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62731be0f22c8c5512da2e8321d0d2cf9aada67f035f520d4a1a03d334a5a3d3`  
		Last Modified: Sat, 26 Jun 2021 01:43:06 GMT  
		Size: 3.6 MB (3644555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451b4aa377b539463494b3469bc28bb1fe25df573a09599376f6f5c3b24addcc`  
		Last Modified: Sat, 26 Jun 2021 01:43:05 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
