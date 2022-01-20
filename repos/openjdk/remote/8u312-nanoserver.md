## `openjdk:8u312-nanoserver`

```console
$ docker pull openjdk@sha256:388556abb06e54739b67f200b47dc5c950b8ed3ec5ecc23329cf6a6713c60568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `openjdk:8u312-nanoserver` - windows version 10.0.17763.2458; amd64

```console
$ docker pull openjdk@sha256:4a1bd3bd998beba3c570dbea92e2173bb7a069d8b628006d15d208a84c3177b7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.3 MB (204301137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef195a35212082088b1adf766725c22730e2a16196684a4448cab5fdae487767`
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
# Wed, 19 Jan 2022 22:40:00 GMT
COPY dir:3a5581b2700e30ac96b7aaa667bdc25cdca1d6451f9f3d58913682ddf8d74e71 in C:\openjdk-8 
# Wed, 19 Jan 2022 22:40:21 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version 	&& echo Complete.
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
	-	`sha256:2f8a7c034e0f6a9355f4d3ac05d156ac7f7b0429f243fd4b72bb442f548dcb35`  
		Last Modified: Thu, 20 Jan 2022 02:44:16 GMT  
		Size: 101.1 MB (101086673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0ae9799efbbb3fa81bd1c0f04fe335b591b211e40e898b96aa7510964acd84`  
		Last Modified: Thu, 20 Jan 2022 02:42:23 GMT  
		Size: 91.5 KB (91521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
