## `openjdk:21-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:bd4416a591321ce46d5b644b744da66646f52360f9317f008106c2561275be6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `openjdk:21-ea-jdk-nanoserver-1809` - windows version 10.0.17763.4010; amd64

```console
$ docker pull openjdk@sha256:545d474ef0b40d77a8df85f50f8f3b92a93807e4ac52444951a7d45dd490367b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304971172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb789ba3513e0e542c3a0dfb13b0b26ee0761e3cf4fa8e8026e933729a891ceb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Feb 2023 10:14:28 GMT
RUN Apply image 10.0.17763.4010
# Wed, 15 Feb 2023 22:46:15 GMT
SHELL [cmd /s /c]
# Thu, 16 Feb 2023 02:20:16 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 16 Feb 2023 02:20:17 GMT
USER ContainerAdministrator
# Thu, 16 Feb 2023 02:20:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 16 Feb 2023 02:20:27 GMT
USER ContainerUser
# Thu, 09 Mar 2023 23:19:44 GMT
ENV JAVA_VERSION=21-ea+13
# Thu, 09 Mar 2023 23:20:01 GMT
COPY dir:2075528fbfcbd8cb9dbdcc1eca298b0afad536273edb6ac4d6a9a87f315425a9 in C:\openjdk-21 
# Thu, 09 Mar 2023 23:20:33 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 09 Mar 2023 23:20:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:00eaf3341cd3cc6b72f91399cb3bd1aba30eb7eead7596532fe54c4bf1b010d7`  
		Last Modified: Thu, 16 Feb 2023 00:31:21 GMT  
		Size: 106.7 MB (106674970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0185f49bd9e9c2d18b1dcf8f1f67123b4146383e07a158cb4623d96fb2d18c05`  
		Last Modified: Thu, 16 Feb 2023 02:29:16 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b040b2f53926e6a02088ae0173e36f1f01b75c581f435607dd2f86dfe095f4a`  
		Last Modified: Thu, 16 Feb 2023 02:29:16 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0134c2e5e080e208ed0917cd948446b60048729433bf731850e4165e426977c`  
		Last Modified: Thu, 16 Feb 2023 02:29:16 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf352af9ffad203bc10ae043af50fee20ca5c0e02a370dcc2b040c702c9d48f`  
		Last Modified: Thu, 16 Feb 2023 02:29:16 GMT  
		Size: 67.9 KB (67900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58adc24996cad294b1ceeed12449ee5750c4442dfcc5e3135984239942ba8503`  
		Last Modified: Thu, 16 Feb 2023 02:29:13 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e537197cee68e173352b768a08a54f013c423c87cd26f82bff9a2d36b2eb2e`  
		Last Modified: Thu, 09 Mar 2023 23:23:23 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15a491b6f03de35c16e2a472c0eb479ecd7b7ce71a749a04dd75acd8fee16c4`  
		Last Modified: Thu, 09 Mar 2023 23:23:45 GMT  
		Size: 194.4 MB (194421812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aaf2849832673baa7229dde200c1a479f6a597c90913291815f4c20a96f6bff`  
		Last Modified: Thu, 09 Mar 2023 23:23:25 GMT  
		Size: 3.8 MB (3799637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813747fa9d8a2fab348d4930ccc1f26803910f1872e0a52af97adb182fd86150`  
		Last Modified: Thu, 09 Mar 2023 23:23:23 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
