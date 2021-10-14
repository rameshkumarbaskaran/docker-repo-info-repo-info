## `eclipse-temurin:16-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:9fc89989628e064ec0cbd2679b9d5a92227cf3a4d990acf5b775870b29e2df65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `eclipse-temurin:16-jdk-nanoserver` - windows version 10.0.17763.2237; amd64

```console
$ docker pull eclipse-temurin@sha256:2cc4d1d5c093a6ce7eff21e9f5d61e43c797306ed270eeae48e10b6f64273866
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.2 MB (305194710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18844d3d83f5bc6d2fc42ca7fd518ea224360024a804907e9e2bc2d7cd77ec44`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Oct 2021 08:01:14 GMT
RUN Apply image 1809-amd64
# Wed, 13 Oct 2021 18:17:55 GMT
SHELL [cmd /s /c]
# Wed, 13 Oct 2021 18:48:35 GMT
ENV JAVA_VERSION=jdk-16.0.2+7
# Wed, 13 Oct 2021 18:48:36 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 13 Oct 2021 18:48:37 GMT
USER ContainerAdministrator
# Wed, 13 Oct 2021 18:48:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Oct 2021 18:48:51 GMT
USER ContainerUser
# Wed, 13 Oct 2021 18:49:12 GMT
COPY dir:9a7ef5975d9ba9576c4744dc049616bbcb218f14c3c0bd967851cd46479d6134 in C:\openjdk-16 
# Wed, 13 Oct 2021 18:49:29 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Oct 2021 18:49:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:934e212983f208dc2bebc5de38259a6a62f1761868aacfee2cb3585a13b1e24b`  
		Size: 102.7 MB (102661372 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ceff24c3c0c2c360cd3788fcde5c41e1d6601339f4944623c732558a6030e631`  
		Last Modified: Wed, 13 Oct 2021 19:12:58 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9eae448fe1c23293a00488f8d588df17a39b2fe8010efb56a969e48984b5ab7`  
		Last Modified: Wed, 13 Oct 2021 19:36:51 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dd3fd488f27f39f39f03c530f1765c8faeb231ef8e947933ded85d931d8f25`  
		Last Modified: Wed, 13 Oct 2021 19:36:51 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846647d37e211454bae54bfbfebc89a65c2db0e349527c3f099a23f38cdc7d0b`  
		Last Modified: Wed, 13 Oct 2021 19:36:51 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ca7b4f4f68d11121da44c6f547ca55b0ad1ab3b9dac1a70d01040feb61b1bd`  
		Last Modified: Wed, 13 Oct 2021 19:36:49 GMT  
		Size: 68.9 KB (68871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6366d67c9d43ba27c68fd782e900f6400606b23827978db2a2097f9d17e5f3`  
		Last Modified: Wed, 13 Oct 2021 19:36:49 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01595522b612bcce3e304cb075e1c321d527b5c45bf8450038437f58ae7bbb35`  
		Last Modified: Wed, 13 Oct 2021 19:40:19 GMT  
		Size: 198.8 MB (198758364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8518791d10f70b1924f19bb4955856be404f68532a0b775f75aac771707ebe0`  
		Last Modified: Wed, 13 Oct 2021 19:36:53 GMT  
		Size: 3.7 MB (3699265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44d836e0d050731f83a0ebe02f5141f78c75fa8b45277baedaaa60b12c55e14`  
		Last Modified: Wed, 13 Oct 2021 19:36:49 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
