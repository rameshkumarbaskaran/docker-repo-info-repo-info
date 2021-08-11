## `openjdk:8u302-nanoserver`

```console
$ docker pull openjdk@sha256:217039a5876f3cf0440cdf7c6d0710baf0325e2bac4c27e35bccf1f65e21f4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `openjdk:8u302-nanoserver` - windows version 10.0.17763.2114; amd64

```console
$ docker pull openjdk@sha256:cee509a35c2380018b79cbd1c22d9603f657be9d696176e36c6821ecd0f418e7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (203958457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d4380d7c725fe629100618b432772bfd2ca00a70c4972e792cbad0091e0620`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Aug 2021 19:15:20 GMT
RUN Apply image 1809-amd64
# Wed, 11 Aug 2021 17:30:38 GMT
SHELL [cmd /s /c]
# Wed, 11 Aug 2021 18:09:04 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 11 Aug 2021 18:09:06 GMT
USER ContainerAdministrator
# Wed, 11 Aug 2021 18:09:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 11 Aug 2021 18:09:24 GMT
USER ContainerUser
# Wed, 11 Aug 2021 18:09:26 GMT
ENV JAVA_VERSION=8u302
# Wed, 11 Aug 2021 18:09:44 GMT
COPY dir:82904e6295068720536f940f57626186b2820e368b810e639bd5a3957d468086 in C:\openjdk-8 
# Wed, 11 Aug 2021 18:10:03 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:bc8517709e9cfff223cb034ff5be8fcbfa5409de286cdac9ae1b8878ebea6b84`  
		Size: 102.7 MB (102741177 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae0a5a946be2ad0e39a8260e454c0060a31a9f7e5be75d1f9038dc13730abc0a`  
		Last Modified: Wed, 11 Aug 2021 18:21:28 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14149e7201b90593d0eab9e2066acc66e8fa43792b932cfbb08532376e34f088`  
		Last Modified: Wed, 11 Aug 2021 18:40:51 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d962baf1cbca863cbaed5a262b5ca0906625c12380c0f74b4bdec6010d95d1`  
		Last Modified: Wed, 11 Aug 2021 18:40:51 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08497a81a0eb54a2594b91f1ac5fb03fb9c3c97da5895abd316e4d9aeb65515d`  
		Last Modified: Wed, 11 Aug 2021 18:40:49 GMT  
		Size: 70.8 KB (70757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33ec46900b40c5f8677e24f9835aede6f7694ea6fe5b6861d6f7689e015e5ab`  
		Last Modified: Wed, 11 Aug 2021 18:40:49 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90276cfc77f6107f01c360f9723106037368c2871eb4165884158e94c8474700`  
		Last Modified: Wed, 11 Aug 2021 18:40:49 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01d187397b348a73f1ad1e4ea2d3efd6d30fd7459843354cb1a357ac1630846`  
		Last Modified: Wed, 11 Aug 2021 18:41:01 GMT  
		Size: 101.0 MB (101049449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c14269da8b664816ab603c2677eee8cd479c3ffe26cb34a7ac21c8abddae8c`  
		Last Modified: Wed, 11 Aug 2021 18:40:49 GMT  
		Size: 91.3 KB (91281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
