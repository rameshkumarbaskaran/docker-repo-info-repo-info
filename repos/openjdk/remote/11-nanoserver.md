## `openjdk:11-nanoserver`

```console
$ docker pull openjdk@sha256:5f81f4d2e988a562f7e7241f9c6a09a7ffdcdbc952e0893f8a915a8914488030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `openjdk:11-nanoserver` - windows version 10.0.17763.3165; amd64

```console
$ docker pull openjdk@sha256:9349ad186fad6a46cf673bd06e21029edc9a27732142e0618c2a10bc86679a37
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294592079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba616272c56f3443e773fb791a6b0b737400a3154ae4157cbe719b38f7101852`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:50:41 GMT
SHELL [cmd /s /c]
# Wed, 13 Jul 2022 16:06:40 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 13 Jul 2022 16:06:41 GMT
USER ContainerAdministrator
# Wed, 13 Jul 2022 16:06:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 Jul 2022 16:06:49 GMT
USER ContainerUser
# Wed, 13 Jul 2022 16:06:50 GMT
ENV JAVA_VERSION=11.0.15
# Wed, 13 Jul 2022 16:07:04 GMT
COPY dir:5ad3e4c4e3ef740d988c27671547403db1e625a1149c18ae86fe9dc1c69b4f23 in C:\openjdk-11 
# Wed, 13 Jul 2022 16:07:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 13 Jul 2022 16:07:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b09c07c6aeead64423fdefc240fe2e1b6330c96732fd2705113030da84416be`  
		Last Modified: Mon, 18 Jul 2022 21:22:33 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1234d8139b62fe1cc2af73e6f7e19087c38bbf27b1301126e4825445a53129ba`  
		Last Modified: Mon, 18 Jul 2022 21:29:22 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fb8775c7c189c574b2c2e9559d8e0069174344caf6a8e82a8a8311e9b46649`  
		Last Modified: Mon, 18 Jul 2022 21:29:22 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48e18300deee27181a3e362a7857b5e4f7d95ad751f96a0b3fff63f97d8ba0f`  
		Last Modified: Mon, 18 Jul 2022 21:29:22 GMT  
		Size: 69.0 KB (68975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31f1cf222f09294611ee30eb57920d0e6ee6e7aecd5a3d0d0ce758b70f63b33`  
		Last Modified: Mon, 18 Jul 2022 21:29:20 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8150b82482f26bc71fcdbb1b6298a2881ddcfca3968939f14bce19e137969245`  
		Last Modified: Mon, 18 Jul 2022 21:29:20 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a31c5a837fcf86a001c49b4b32175466d8cd8aec3529f4f79b7718ad584f84`  
		Last Modified: Mon, 18 Jul 2022 21:29:40 GMT  
		Size: 191.3 MB (191278907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e382effdbe058be630aafa6a0c25e541b6247ce204b143a9f1c4e062fe32aaf`  
		Last Modified: Mon, 18 Jul 2022 21:29:20 GMT  
		Size: 82.3 KB (82290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1232d74594e9a894fe9c9128e69eb9b63e358b0b2c52f5cf5fcbe388299afd59`  
		Last Modified: Mon, 18 Jul 2022 21:29:19 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
