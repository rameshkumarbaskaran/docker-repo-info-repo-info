## `openjdk:18-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:912c0fa3d8c379c8e026b7fb1cb1876df6df8917737eaa408c126d50a0b004f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `openjdk:18-ea-jdk-nanoserver` - windows version 10.0.17763.1999; amd64

```console
$ docker pull openjdk@sha256:b150452a179289a3d36dd6eaa6c551a0035ee001cdc9e231937150f6317e3235
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289369521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c972eb2f0ed7491980bf33497042bde0fb911027aabe93bdd7078e9cd6e309`
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
# Tue, 22 Jun 2021 21:21:58 GMT
ENV JAVA_VERSION=18-ea+2
# Tue, 22 Jun 2021 21:22:17 GMT
COPY dir:c330d3977d26b0294f60bff63d271375a1f93464967a1747f2e1b352b1214d79 in C:\openjdk-18 
# Tue, 22 Jun 2021 21:23:00 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 22 Jun 2021 21:23:03 GMT
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
	-	`sha256:40f543ba83256c5fe5e6df6ee38e4b36449fec83266e0bdb650af355e4cb5a7a`  
		Last Modified: Tue, 22 Jun 2021 21:37:28 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123c989772f15e0dcb5345563dfc0b753962cd283648a8d22c379d6e0528265f`  
		Last Modified: Tue, 22 Jun 2021 21:37:49 GMT  
		Size: 183.0 MB (182981468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079362e5b0984b748c968a7156dbb9c2338a749ad7a347951eb75511350255c5`  
		Last Modified: Tue, 22 Jun 2021 21:37:30 GMT  
		Size: 3.6 MB (3642215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f88ed9cb26a7c81face21e8f7499a11d81ab6a0e063466fd537d45783e040d`  
		Last Modified: Tue, 22 Jun 2021 21:37:28 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
