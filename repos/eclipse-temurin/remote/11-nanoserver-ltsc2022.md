## `eclipse-temurin:11-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:19b51932dbe596a8b09cf974d4669fe7776d8da9302463d3297855d2083c12cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `eclipse-temurin:11-nanoserver-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull eclipse-temurin@sha256:7267b6252589f74fcd53bb674d0a69937425ab0820ed9de509749dc089d5d530
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313754753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb75b4c99114bdb6823f4c2ad02752244ce992109e24b7871e8034cc43297577`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Aug 2023 09:40:19 GMT
RUN Apply image 10.0.20348.1906
# Thu, 10 Aug 2023 00:11:36 GMT
SHELL [cmd /s /c]
# Thu, 31 Aug 2023 20:35:19 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Thu, 31 Aug 2023 20:35:19 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 31 Aug 2023 20:35:20 GMT
USER ContainerAdministrator
# Thu, 31 Aug 2023 20:35:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 31 Aug 2023 20:35:35 GMT
USER ContainerUser
# Thu, 31 Aug 2023 20:35:51 GMT
COPY dir:bc17122f89ccac6825b72157f71faf8ee914101def60109a37803e17ec7fe7f6 in C:\openjdk-11 
# Thu, 31 Aug 2023 20:36:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 20:36:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea9613880997b3ab2284a37c0c14a403553457b0c331b41c6bd6d1cc7838a222`  
		Last Modified: Tue, 08 Aug 2023 18:47:21 GMT  
		Size: 120.5 MB (120500677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3572ac06c9147f0946a40530f2197bb0101b82dd45b1defe04a8904a1c81a18`  
		Last Modified: Thu, 10 Aug 2023 00:30:45 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61035630ec034b6bf9a07ea89a5c642bbfda6cde07b3a961806f3f1edd757d4e`  
		Last Modified: Thu, 31 Aug 2023 20:46:16 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76245a0f0f68458fd331220ea5ab8cc6c9348f9bc1b695cd1dab69fbdae54623`  
		Last Modified: Thu, 31 Aug 2023 20:46:16 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93764e3ebb3781d3ab774eeefd4593d9cc4a3c62c408a4c606fb2e027e9ee49e`  
		Last Modified: Thu, 31 Aug 2023 20:46:15 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644c458ef263d3e844dda1b073c51b7182c392fb16bbb5fb6e7180db39f40bff`  
		Last Modified: Thu, 31 Aug 2023 20:46:14 GMT  
		Size: 80.1 KB (80146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6229cb497f63e937da0a8fe8a9311469c5dc2fdc9500fcbeb2666bbfe783db06`  
		Last Modified: Thu, 31 Aug 2023 20:46:13 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff258607c509cb026668a9dd6171d9cc8ab7f667e078debdf3b29de8d3d71b6f`  
		Last Modified: Thu, 31 Aug 2023 20:46:31 GMT  
		Size: 193.1 MB (193105613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbc24ed6087d11f054f6fbbcad7fd54af3dad1d674b07a5060f2087c7a9eb06`  
		Last Modified: Thu, 31 Aug 2023 20:46:13 GMT  
		Size: 62.0 KB (61972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73272bdbbf2362be410b0399c41c817a260bd4082c2c6a2997ab8f955cdb0c71`  
		Last Modified: Thu, 31 Aug 2023 20:46:14 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
