## `openjdk:11-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:d25048f86d13be53b435963e9aa17bafe95051b0cab4942cee30d2afc8fa64b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `openjdk:11-jre-nanoserver-1809` - windows version 10.0.17763.1040; amd64

```console
$ docker pull openjdk@sha256:184c3ab79c027c91aaec40a4a809c5a0a7bf11b4782bb512b0a4f9fc9923e063
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.2 MB (291170393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bda546e9302eeb9c24cc63d23eeb19c177ef4f4819f8d759fd1ec970612535`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 16 Feb 2020 01:25:57 GMT
RUN Apply image 1809-amd64
# Thu, 20 Feb 2020 02:05:49 GMT
SHELL [cmd /s /c]
# Thu, 20 Feb 2020 02:43:06 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 20 Feb 2020 02:43:07 GMT
USER ContainerAdministrator
# Thu, 20 Feb 2020 02:43:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Thu, 20 Feb 2020 02:43:20 GMT
USER ContainerUser
# Thu, 20 Feb 2020 02:43:21 GMT
ENV JAVA_VERSION=11.0.6
# Thu, 20 Feb 2020 02:44:22 GMT
COPY dir:dcc02c643f10bd08676197988d11abdf4d8aeda19e024c3b8c403d1d777f4b34 in C:\openjdk-11 
# Thu, 20 Feb 2020 02:48:40 GMT
RUN echo Verifying install ... 	&& echo   java --version && java --version
```

-	Layers:
	-	`sha256:a35da61c356213336e646756218539950461ff2bf096badf307a23add6e70053`  
		Size: 101.1 MB (101145811 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:141e7d00d8743fe3d0c951c1f46529a11bff09056f891a37a603bbde2491228e`  
		Last Modified: Thu, 20 Feb 2020 03:06:23 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96f315b3bca76990765638c51ae018eb1d1a673047e1829e7d4a4d698657f22`  
		Last Modified: Thu, 20 Feb 2020 03:27:30 GMT  
		Size: 939.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a52f396ea03e24174fc0f51b3c421b9a607598d3773234b218e62cb07e8d44`  
		Last Modified: Thu, 20 Feb 2020 03:27:30 GMT  
		Size: 940.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68a3510380a2d9374605533996b2455c9cdf9ea293018dbfd5dd69f3fc8c2cf`  
		Last Modified: Thu, 20 Feb 2020 03:27:30 GMT  
		Size: 72.3 KB (72283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e52c7397d4b034a18e6685068a14c08f88d1d9d6fc693bb36bf7ca934c11938`  
		Last Modified: Thu, 20 Feb 2020 03:27:28 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5a81a75f004ff028e6d095cc79fb05a2ecbe6c9cd87b1168b2fbc70b3b4e9d`  
		Last Modified: Thu, 20 Feb 2020 03:27:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02561438d932565010a2a4360d785c161a193c5efc529c2a76a1d9a29678c182`  
		Last Modified: Thu, 20 Feb 2020 03:27:55 GMT  
		Size: 189.9 MB (189905667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ea81cb99ff2e625028c657482ece540984fc97121ff76dcbddbba297184922`  
		Last Modified: Thu, 20 Feb 2020 03:30:23 GMT  
		Size: 42.0 KB (41958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
