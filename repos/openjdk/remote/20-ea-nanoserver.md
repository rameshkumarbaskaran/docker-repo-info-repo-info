## `openjdk:20-ea-nanoserver`

```console
$ docker pull openjdk@sha256:4413042b25f5494e8168b68379abd616f9659b540f1f39c6b8ddfbf036cea3fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `openjdk:20-ea-nanoserver` - windows version 10.0.17763.3287; amd64

```console
$ docker pull openjdk@sha256:d0bd42b7cccc77bfa5d6cf16c2f4718b1dbe58087f6a58e94fd7432dfb8df280
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.3 MB (299326010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb1caee3801af5211ec7418ed98533fc905cb1bf90a7a4eb25618c2072d5907`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:57:07 GMT
SHELL [cmd /s /c]
# Wed, 10 Aug 2022 17:00:08 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 10 Aug 2022 17:00:09 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 17:00:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Aug 2022 17:00:18 GMT
USER ContainerUser
# Fri, 26 Aug 2022 22:18:45 GMT
ENV JAVA_VERSION=20-ea+12
# Fri, 26 Aug 2022 22:19:01 GMT
COPY dir:66236f68be4cd54a3db7ed3d4aecc73eec22dbccd58a43076cd3fcdbc29f9289 in C:\openjdk-20 
# Fri, 26 Aug 2022 22:19:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 26 Aug 2022 22:19:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0f4438539876006761cb687527bd8cb94cc7a273cf8bb47563981044f2e1771e`  
		Last Modified: Wed, 10 Aug 2022 16:38:40 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151c855f0d179e8547473b92e962fb22b468853448fe0849dadde3526c52aceb`  
		Last Modified: Wed, 10 Aug 2022 17:28:35 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3386f9f9687d0a909a16379459e37c52a2de2070297d81d4167037a0602e3e86`  
		Last Modified: Wed, 10 Aug 2022 17:28:35 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28092505f98fc516238306cba539a3a8a6d7f48ca19dc6e6c3cca668dc6f466c`  
		Last Modified: Wed, 10 Aug 2022 17:28:35 GMT  
		Size: 75.6 KB (75615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfea14a612ecceac1dd16eaa1da4863923aa41d796fd4f9c1fae46d918d4299`  
		Last Modified: Wed, 10 Aug 2022 17:28:33 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf639a34d85f4c664671b24e279f3d6f4fa3ed7878d37831d453c35d3483e550`  
		Last Modified: Fri, 26 Aug 2022 22:23:04 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c879ae59a20a5caf50be8e75a6b8139e4fce4758c42dc9864b427902caa6323a`  
		Last Modified: Fri, 26 Aug 2022 22:23:25 GMT  
		Size: 192.3 MB (192324823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698f2f2fd52a9eaf13e2a3fd3caf6e45b2b8cba051d28fdfe1ca9dd0eee0a223`  
		Last Modified: Fri, 26 Aug 2022 22:23:05 GMT  
		Size: 3.7 MB (3714474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ac2fff06498122a69215f1c8f8cc0a5c45e9f4532cfde005c0b1e32ebfc7df`  
		Last Modified: Fri, 26 Aug 2022 22:23:04 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
