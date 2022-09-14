## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:1ce66c08c29d5d1544e6337538e07bcd77653b765e28ca03a9732e0eab379f4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:9a65eb76588c33bfe547549c9a9c4adc0864389eb63832624c860693ca49f65b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161523523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f768401b445f32404278f8842c4c776cbf96eb6a36ceeedfbeabd0e3a8c33e99`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Sep 2022 20:11:22 GMT
RUN Apply image 10.0.20348.1006
# Wed, 14 Sep 2022 16:38:20 GMT
SHELL [cmd /s /c]
# Wed, 14 Sep 2022 16:41:02 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Wed, 14 Sep 2022 16:41:02 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 14 Sep 2022 16:41:03 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 16:41:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Sep 2022 16:41:13 GMT
USER ContainerUser
# Wed, 14 Sep 2022 16:42:02 GMT
COPY dir:b68e969b54b81d301cc08056fc3e121f2bd91a79ba6f45c80e26c9a9bf23468d in C:\openjdk-17 
# Wed, 14 Sep 2022 16:42:17 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:09629875cd6ee57fa551626fa2963d8b54718ba9acbf28e7cb5d684a9cb754d7`  
		Size: 118.1 MB (118131331 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:07f30e2ceaa03f6ac7b6e6f319083288f48d1fa2a61f36f51f516da241496976`  
		Last Modified: Wed, 14 Sep 2022 16:57:28 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366e22b303e937ccca7ee1049d6ff7499f528205ccb591a0d932cf3252addc06`  
		Last Modified: Wed, 14 Sep 2022 16:58:59 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e70bf43cde7b760ac8122291c367c2cc47128dd9634074494e86fa7fc37610`  
		Last Modified: Wed, 14 Sep 2022 16:58:59 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ac186b5d9d2033189bf6ee16975920dcc36b8b08058845955f692fc8b9b2ac`  
		Last Modified: Wed, 14 Sep 2022 16:58:59 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ebb961fc182cafd24a1f77bdf2e7fc3ca4d49e28e496c7f2a423955d77eaf3`  
		Last Modified: Wed, 14 Sep 2022 16:58:57 GMT  
		Size: 83.4 KB (83375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3efa23416ae67d7e3cd23faca9709537fbf9ba5914ab51f11f32209e6928418`  
		Last Modified: Wed, 14 Sep 2022 16:58:57 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c250029d1a4b3e0bb17cb6796f4772b8a75a093d79466de6beb28db4fde6dc7f`  
		Last Modified: Wed, 14 Sep 2022 16:59:38 GMT  
		Size: 43.2 MB (43231035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089a3cc594cdd98062f866199e5794992d3f9655ffdda4bf32fa1c3ad2e61ba1`  
		Last Modified: Wed, 14 Sep 2022 16:59:30 GMT  
		Size: 72.6 KB (72611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.3406; amd64

```console
$ docker pull eclipse-temurin@sha256:d69c2d88edc0df5278fdc311c949a4ebd5eac9e8ba406819752c4ead63881059
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.7 MB (149673891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42cd9ff7f3be190c82edcac19af827c19ddf3113bb48a5e59a2b504b3acc5cbd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 16:03:00 GMT
SHELL [cmd /s /c]
# Wed, 14 Sep 2022 16:21:28 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Wed, 14 Sep 2022 16:21:29 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 14 Sep 2022 16:21:29 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 16:21:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Sep 2022 16:21:40 GMT
USER ContainerUser
# Wed, 14 Sep 2022 16:26:08 GMT
COPY dir:b68e969b54b81d301cc08056fc3e121f2bd91a79ba6f45c80e26c9a9bf23468d in C:\openjdk-17 
# Wed, 14 Sep 2022 16:26:23 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:233f09b2a52487084f2cfb5e06dac2815651432c9d37c729582f59cfcf66b243`  
		Last Modified: Wed, 14 Sep 2022 16:47:12 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdc7267fe495d0cdf992be53b1fdd69c7c1ed0a3e2840762d8c5bb92c68a753`  
		Last Modified: Wed, 14 Sep 2022 16:52:48 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43f85722444dd97028b181a698b832b9c51cfcd6f12661ec22dec74858a8f3c`  
		Last Modified: Wed, 14 Sep 2022 16:52:48 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea208f743e3b8c0d1ba8973b583d6578c9c0cd9dfe02acce5e09a10df9c30bc`  
		Last Modified: Wed, 14 Sep 2022 16:52:48 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a00d33598c1ee2a4429cfa620e2bd5d1017c1c00b27c156856223f0c81bcbe3`  
		Last Modified: Wed, 14 Sep 2022 16:52:46 GMT  
		Size: 70.9 KB (70902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31aa2d6995a907d4a4fa5322a9d74f1c3f9548fe6a7f975a846b96aa5c6b603`  
		Last Modified: Wed, 14 Sep 2022 16:52:46 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0421d04fa2ee0d1eeb714212adc6becee4d9d77908f0f3468e2bee2bc5a89c1d`  
		Last Modified: Wed, 14 Sep 2022 16:54:15 GMT  
		Size: 43.2 MB (43228734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fc8a65b1968b41a5eeae7c06db79c598b98e80840925f1cb67cad3bc80248f`  
		Last Modified: Wed, 14 Sep 2022 16:54:07 GMT  
		Size: 3.0 MB (3034326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
