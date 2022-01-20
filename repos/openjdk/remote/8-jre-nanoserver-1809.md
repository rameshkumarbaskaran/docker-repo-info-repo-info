## `openjdk:8-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:6a5efbfc2dd4b00bb120f8f57e2b112fd08d2ec63a69f9e4c1cf0970e1a5e63b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `openjdk:8-jre-nanoserver-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull openjdk@sha256:53f62c7584d3a1c99aa7d65e94c2844da705270b544aef1d2492ba4ec6e0cb1a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141451428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69dafd4df47f36b6204d08eec422eb3f7fcc6db6bc8f65285dd4dedd6baf52e0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 19 Jan 2022 22:25:45 GMT
SHELL [cmd /s /c]
# Wed, 19 Jan 2022 22:39:29 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 19 Jan 2022 22:39:30 GMT
USER ContainerAdministrator
# Wed, 19 Jan 2022 22:39:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 19 Jan 2022 22:39:39 GMT
USER ContainerUser
# Wed, 19 Jan 2022 22:39:40 GMT
ENV JAVA_VERSION=8u312
# Wed, 19 Jan 2022 22:41:33 GMT
COPY dir:d01eca1f47b40119ea7401e87f8309ebbb3c59555f496ebfb4562b12d58cd948 in C:\openjdk-8 
# Wed, 19 Jan 2022 22:41:47 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a1b3e13bb7b3d4b61b5f49a91d6eb9bfcf5539ab89c3687d608f17713c2409b5`  
		Last Modified: Thu, 20 Jan 2022 02:21:30 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338bf0e38fb7f2b8a0fb5e7eb7fab0a55b72f807f8f29e8a8cca893d27d9a3a8`  
		Last Modified: Thu, 20 Jan 2022 02:42:25 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad2e28cd185f66eb0db90aedacf18508ccfd1a587b64c68b818e6a6ccf36580`  
		Last Modified: Thu, 20 Jan 2022 02:42:25 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8734a1268ea949016e9c473f5bdb78cb61ed8fe90ee65b5ba7b2ebd765496205`  
		Last Modified: Thu, 20 Jan 2022 02:42:23 GMT  
		Size: 70.7 KB (70719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d88295d21d31aa302a0382ecc8affcdb2d99175e66a11a9467f383a411d75e`  
		Last Modified: Thu, 20 Jan 2022 02:42:23 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3c7a733c82f9375d4f846ad762da60a5ae2a11133e007f57c5d5af8c54a1fb`  
		Last Modified: Thu, 20 Jan 2022 02:42:23 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc895b195bcd81d8ebc55650d018bb68b23d92efbc0150faddd5b06dea03b2d5`  
		Last Modified: Thu, 20 Jan 2022 02:45:48 GMT  
		Size: 38.2 MB (38246425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afef8744d75328734d52bca117fceaf082dd48f9c3ce95283e1e01ea8ba24677`  
		Last Modified: Thu, 20 Jan 2022 02:45:08 GMT  
		Size: 82.1 KB (82060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
