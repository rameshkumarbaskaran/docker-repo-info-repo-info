## `openjdk:8u242-jre-nanoserver`

```console
$ docker pull openjdk@sha256:d2003910883aa935478143e14723bbd9680f91dd3c7bc30ea25c98408a500553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `openjdk:8u242-jre-nanoserver` - windows version 10.0.17763.1040; amd64

```console
$ docker pull openjdk@sha256:c086c3f018ac33e21a13d47a44c5a79c3a3879bef4192a44bc2ab4d20a5e3b95
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 MB (200770403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7599df234eea4a4276293e4055383cc4749e42c3cae6a87104e73e45dcca15`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 16 Feb 2020 01:25:57 GMT
RUN Apply image 1809-amd64
# Thu, 20 Feb 2020 02:05:49 GMT
SHELL [cmd /s /c]
# Thu, 20 Feb 2020 02:55:38 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 20 Feb 2020 02:55:39 GMT
USER ContainerAdministrator
# Thu, 20 Feb 2020 02:55:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Thu, 20 Feb 2020 02:55:53 GMT
USER ContainerUser
# Thu, 20 Feb 2020 02:55:54 GMT
ENV JAVA_VERSION=8u242
# Thu, 20 Feb 2020 02:56:39 GMT
COPY dir:604850e4892a2e6375b4d95fb378e9776042497a20a33de1bbe6b0d17fade1d2 in C:\openjdk-8 
# Thu, 20 Feb 2020 03:00:36 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version
```

-	Layers:
	-	`sha256:a35da61c356213336e646756218539950461ff2bf096badf307a23add6e70053`  
		Size: 101.1 MB (101145811 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:141e7d00d8743fe3d0c951c1f46529a11bff09056f891a37a603bbde2491228e`  
		Last Modified: Thu, 20 Feb 2020 03:06:23 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6176fdaebd5f963182cc25520a3622bafe55a2287af69b86c1e228457a23ae56`  
		Last Modified: Thu, 20 Feb 2020 03:33:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8fa4840f774e77986a944d59d4a70b9ba4c2517b10f15dfbe8da84f4813437`  
		Last Modified: Thu, 20 Feb 2020 03:33:11 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34101f5fc575ed171f2b20a67bba2d4a7886b13914c382e028ebd45052acc5ae`  
		Last Modified: Thu, 20 Feb 2020 03:33:08 GMT  
		Size: 66.1 KB (66063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8487456a6048dabff36855724b6e8b0122de0f5491c9350c4de470fd114b3ea0`  
		Last Modified: Thu, 20 Feb 2020 03:33:08 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a1696d652af6514494ecf276fe0490f3047e25aea67972fcab674add23c4b8`  
		Last Modified: Thu, 20 Feb 2020 03:33:08 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402a454cbe88ce86069fa8b0ce3473dbfd2852cac5dc02f9b582eb447c143020`  
		Last Modified: Thu, 20 Feb 2020 03:33:24 GMT  
		Size: 99.5 MB (99476004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459799a5621ee1e44a36f674d7d6eebcb8d9a472776dc0706eb942bf0ad28626`  
		Last Modified: Thu, 20 Feb 2020 03:35:10 GMT  
		Size: 77.9 KB (77858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
