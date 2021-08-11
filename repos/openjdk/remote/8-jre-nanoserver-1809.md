## `openjdk:8-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:8186bb0f10c346a7e9c7c3528ac5ba5d76085d787074fc87ff54bc166abbbcb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `openjdk:8-jre-nanoserver-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull openjdk@sha256:6f182e92e917dd43f608f1f68d72d16cd213fb4e3dc4dd31f6ac478cae3eef47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141121949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed49b7c479d004220dce5c2c485acace26c953cb5975700119b6b91d9974ad91`
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
# Wed, 11 Aug 2021 18:13:46 GMT
COPY dir:58006f68c4ea109e560c76de14918bddd55bac9724011203b6cdeb031fa20971 in C:\openjdk-8 
# Wed, 11 Aug 2021 18:14:04 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version 	&& echo Complete.
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
	-	`sha256:7258c2cbf5d740979ff1b4ea3a17deb2b5e403b8582cb625c406d5dc073ac369`  
		Last Modified: Wed, 11 Aug 2021 18:43:19 GMT  
		Size: 38.2 MB (38222138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38c94cd9533430f66b8ab251a5add31eae4273fa859d583230c66535de46ca6`  
		Last Modified: Wed, 11 Aug 2021 18:42:37 GMT  
		Size: 82.1 KB (82084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
