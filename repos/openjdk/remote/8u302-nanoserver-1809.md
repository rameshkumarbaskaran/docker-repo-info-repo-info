## `openjdk:8u302-nanoserver-1809`

```console
$ docker pull openjdk@sha256:eecac80bf1f774fca51f05783a8832db484a6cf3f0238b0cb786f2432539c7fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `openjdk:8u302-nanoserver-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull openjdk@sha256:2863f64a28bfe63ca4168c6fda533c3580982afa9941dae89568f8cc1db5b16d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203890393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d479e17fd3fbe5c1bf7fd1622fc85d44d6fda8f32d9cbc7b97e60835812272`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 00:38:23 GMT
SHELL [cmd /s /c]
# Wed, 15 Sep 2021 01:03:44 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Sep 2021 01:03:45 GMT
USER ContainerAdministrator
# Wed, 15 Sep 2021 01:03:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 15 Sep 2021 01:03:53 GMT
USER ContainerUser
# Wed, 15 Sep 2021 01:03:54 GMT
ENV JAVA_VERSION=8u302
# Wed, 15 Sep 2021 01:04:08 GMT
COPY dir:82904e6295068720536f940f57626186b2820e368b810e639bd5a3957d468086 in C:\openjdk-8 
# Wed, 15 Sep 2021 01:04:18 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:807d06303c39b2317729754a4c7ad6501e59c16ee464f8f671f9947774f62f72`  
		Last Modified: Wed, 15 Sep 2021 01:10:56 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599e1258c31953f5f847484fb4c37a5bbc5b30a8a1555a7df2c1ff0e68b8ab93`  
		Last Modified: Wed, 15 Sep 2021 01:27:41 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed51cbf293591feeb6061aad188ab2cd41ac2d2f2e8c3a6858f8d6ba5377879`  
		Last Modified: Wed, 15 Sep 2021 01:27:41 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108d571bf68a07dc3c753512d7c1a67976307f9b650af9346719c4f62e41978d`  
		Last Modified: Wed, 15 Sep 2021 01:27:39 GMT  
		Size: 75.1 KB (75110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bf35bf6b36e006f9f20bf2f357cf98aff5bb2f66714383e0bd8394e9b32ca8`  
		Last Modified: Wed, 15 Sep 2021 01:27:38 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881fd4df3e13c64dc1cf1e7681e90e5cc0755381eaecc694d370ba343f271fa7`  
		Last Modified: Wed, 15 Sep 2021 01:27:38 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c87c908fa6838f6dee67c03a821e4fad8a925debe6f3a1cb63089cb13588e1`  
		Last Modified: Wed, 15 Sep 2021 01:27:49 GMT  
		Size: 101.1 MB (101058384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bab2f9c15a848074b9a3bea590771419779669036a3802ec848a9d6c6c10d7`  
		Last Modified: Wed, 15 Sep 2021 01:27:39 GMT  
		Size: 47.9 KB (47850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
