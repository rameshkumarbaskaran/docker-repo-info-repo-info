## `openjdk:18-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:163fcf3695a26776d8d199d70fcfc9d2a158f471c29a08309d3459fa02941e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `openjdk:18-jdk-nanoserver` - windows version 10.0.17763.2565; amd64

```console
$ docker pull openjdk@sha256:22292684c0974f005fab5fab7e2e1ac79a02325a5709d37bb45d093474163b4c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.7 MB (290689397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df7151a01df02ab3dead45d0cd2179fb0efc201ea5b3d79d5f1beb462ba758b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:45:32 GMT
SHELL [cmd /s /c]
# Wed, 09 Feb 2022 18:51:12 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 09 Feb 2022 18:51:13 GMT
USER ContainerAdministrator
# Wed, 09 Feb 2022 18:51:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Feb 2022 18:51:21 GMT
USER ContainerUser
# Mon, 21 Feb 2022 18:22:48 GMT
ENV JAVA_VERSION=18
# Mon, 21 Feb 2022 18:23:02 GMT
COPY dir:9514de164eda2cdb5e3ddd51197372d790fb5291cfc39842e090e2c568516144 in C:\openjdk-18 
# Mon, 21 Feb 2022 18:23:23 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 21 Feb 2022 18:23:24 GMT
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
	-	`sha256:cadac251c3aa431173a9a814bbf22a1c4c7cc50c68fe4a5f5b4592a6f7eb2ab5`  
		Last Modified: Wed, 09 Feb 2022 19:22:54 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe9859cca3203f733180120b02358ffe6dcf5529a6f520497fc7c9b10faee52`  
		Last Modified: Wed, 09 Feb 2022 19:22:54 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a2fdc8fc9937a202c512de06d672695c8ab28ea5e9dc2713829471e0624e6a`  
		Last Modified: Wed, 09 Feb 2022 19:22:54 GMT  
		Size: 75.1 KB (75096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984c82eb4195ae947a96ff3d0c602b4ade866b01484e6e1b42f60f69163cecbc`  
		Last Modified: Wed, 09 Feb 2022 19:22:51 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76445a11eecab0e84b75c16528b32fb3912f22e0643e2cc6d6c8de95bc67f08f`  
		Last Modified: Mon, 21 Feb 2022 19:32:21 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae32b6f5818679a93b78d52da5919a298b5eb6321191dc25d7fae3dece49b76`  
		Last Modified: Mon, 21 Feb 2022 19:32:44 GMT  
		Size: 184.0 MB (183970691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57890f0680971ea57912a01fe26dcd234b141d1104d75fcf1d256123c68090ed`  
		Last Modified: Mon, 21 Feb 2022 19:32:22 GMT  
		Size: 3.5 MB (3549551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ebc941f374dd745b30387ee606d343d507545741a79102842fe442c3e9f2921`  
		Last Modified: Mon, 21 Feb 2022 19:32:21 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
