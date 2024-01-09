## `openjdk:23-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:7c783b8a337af4308cd81532a4ed8fb80356a27190470c8fcb384397f04b4c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `openjdk:23-ea-jdk-nanoserver-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull openjdk@sha256:ac1f21b7acd6ca8406e456f8fa25bda58f7abee4f73c04d49d35c6b376a16afc
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 MB (305840776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba9aa88931865caf39ca4dd0a6476b6c017c83f192ed8b9ea9f27f8ab4631b4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Dec 2023 10:54:04 GMT
RUN Apply image 10.0.17763.5206
# Tue, 09 Jan 2024 02:48:24 GMT
SHELL [cmd /s /c]
# Tue, 09 Jan 2024 02:48:26 GMT
ENV JAVA_HOME=C:\openjdk-23
# Tue, 09 Jan 2024 02:48:27 GMT
USER ContainerAdministrator
# Tue, 09 Jan 2024 02:48:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 09 Jan 2024 02:48:43 GMT
USER ContainerUser
# Tue, 09 Jan 2024 02:48:44 GMT
ENV JAVA_VERSION=23-ea+4
# Tue, 09 Jan 2024 02:48:53 GMT
COPY dir:b1dbdc77fa994774cb71fa9af312b9dd09b92bbbdd1998ea80c5705205a8768a in C:\openjdk-23 
# Tue, 09 Jan 2024 02:48:59 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 09 Jan 2024 02:49:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:424f13a93a185a5defe848e7d270655e05233555f51328c0af24b9e70677d037`  
		Last Modified: Tue, 12 Dec 2023 20:02:40 GMT  
		Size: 104.5 MB (104510104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fddd9f22df926c51a08c3b6b159992458c3c0f172069f2c8680638dd49a4082f`  
		Last Modified: Tue, 09 Jan 2024 02:49:06 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d82e1b13350578b6f5bcb3a8ea1c5dfc2fc920a89e5bf9124af0ef5bbbc0c7a`  
		Last Modified: Tue, 09 Jan 2024 02:49:05 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b66e8247b91c46e71c9cce9f53a418fcaf3de07e418bba00e751cff290b1f61`  
		Last Modified: Tue, 09 Jan 2024 02:49:04 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb80a179d4cc45bdf199712d5e05408cd5612a9a7d6eef940b828be96c6d28d5`  
		Last Modified: Tue, 09 Jan 2024 02:49:04 GMT  
		Size: 67.0 KB (66975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8de383dbf5cf382ea03dee50bcfd397948d6d0c5492f63237ae641995fd5e46`  
		Last Modified: Tue, 09 Jan 2024 02:49:03 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4aa41659171f32f940f6c78df2eb40e008399775a7a38905e12fd6a8315221`  
		Last Modified: Tue, 09 Jan 2024 02:49:03 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235a2e4ce8162fc8b5dff01b05f200f3a06bce28e2642d0316e0ed830503b8fa`  
		Last Modified: Tue, 09 Jan 2024 02:49:15 GMT  
		Size: 197.4 MB (197426810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c149f36d02f34c8ca47c942848b83a4733a7f6e128907fce8a9ff6a5345f87`  
		Last Modified: Tue, 09 Jan 2024 02:49:04 GMT  
		Size: 3.8 MB (3830558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94144f454b510f7bed1bc3524f09ce763599251677a422a362e3345b04630cf8`  
		Last Modified: Tue, 09 Jan 2024 02:49:03 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
