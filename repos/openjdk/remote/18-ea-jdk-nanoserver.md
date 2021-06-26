## `openjdk:18-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:b4c095157a7e325547aa3e792bd11b3dde1d858e4159ac928c563b6884437409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `openjdk:18-ea-jdk-nanoserver` - windows version 10.0.17763.1999; amd64

```console
$ docker pull openjdk@sha256:51d584f00f41a7ee243d95a9503ac2694519e9482784fd0b22f4d6f1313702db
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289346964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3b7f0e23265ce4ae60226038fb3c47e6cbe2d30a84bb9745507cb0901c680d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 16:52:42 GMT
SHELL [cmd /s /c]
# Mon, 14 Jun 2021 21:23:18 GMT
ENV JAVA_HOME=C:\openjdk-18
# Mon, 14 Jun 2021 21:23:21 GMT
USER ContainerAdministrator
# Mon, 14 Jun 2021 21:23:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 14 Jun 2021 21:23:49 GMT
USER ContainerUser
# Sat, 26 Jun 2021 01:29:02 GMT
ENV JAVA_VERSION=18-ea+3
# Sat, 26 Jun 2021 01:29:21 GMT
COPY dir:1bf98e873db6f23582ed43d3a087a9d75e9fd769a879c6714d7addd6f7f2f480 in C:\openjdk-18 
# Sat, 26 Jun 2021 01:29:53 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 26 Jun 2021 01:29:56 GMT
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
	-	`sha256:38a8aa554907fcec99de91851053bfbdcc543f546430c0a1c27a0354cf66ab24`  
		Last Modified: Mon, 14 Jun 2021 21:39:04 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912c2d7b4763a54931ac01e61f4d52cf9bdfbcb35903c8a29acbc422174b5197`  
		Last Modified: Mon, 14 Jun 2021 21:39:04 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b175b01ffc1eae821eef4878d9ba8edc445669d64945462f128e7caa1a5cbb3`  
		Last Modified: Mon, 14 Jun 2021 21:39:04 GMT  
		Size: 67.8 KB (67770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696d5b17d363cf6c1471c63b7fc24a3d3c36b15d702a96f0f4ce1cdf249db20f`  
		Last Modified: Mon, 14 Jun 2021 21:39:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344cf52e05961f5be8a41dbe2fae40a61d43df91cf41c1ea3993007d85b04959`  
		Last Modified: Sat, 26 Jun 2021 01:41:02 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064d8042de0cbefa28eccb6141a83fe1f116539a7bb47f37da93ad265dc37722`  
		Last Modified: Sat, 26 Jun 2021 01:41:23 GMT  
		Size: 183.0 MB (182957626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce77755f39752f6f1485adea067813fa61b0c38ab58b62c55fe0eb81b7048be`  
		Last Modified: Sat, 26 Jun 2021 01:41:04 GMT  
		Size: 3.6 MB (3643549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf91f08c26e979174d0fafa8f76ca271ebcbd0f439305312010a8c4e3cfd3d9`  
		Last Modified: Sat, 26 Jun 2021 01:41:02 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
