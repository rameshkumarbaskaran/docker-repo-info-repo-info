## `eclipse-temurin:17-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:c0992832ec0bea486e39791f9bee8e9cc93b0aa8962789e784ce5d33236f36e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull eclipse-temurin@sha256:02cd9630b39327a0f9aaf0de2e6570859443da50d7e01f9968dc8640c8490102
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306373555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a545c3b976bf787cc03f2b6caecc7c1b8fe39f84b353a28ce903cf566e845cf5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Aug 2023 09:40:19 GMT
RUN Apply image 10.0.20348.1906
# Thu, 10 Aug 2023 00:11:36 GMT
SHELL [cmd /s /c]
# Thu, 31 Aug 2023 20:36:45 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Thu, 31 Aug 2023 20:36:46 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 31 Aug 2023 20:36:46 GMT
USER ContainerAdministrator
# Thu, 31 Aug 2023 20:36:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 31 Aug 2023 20:36:57 GMT
USER ContainerUser
# Thu, 31 Aug 2023 20:37:12 GMT
COPY dir:87d4868aeffb4665dc24a8514128e3f1a9351c7c90320c533fd29622fc9de6e2 in C:\openjdk-17 
# Thu, 31 Aug 2023 20:37:26 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 20:37:26 GMT
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
	-	`sha256:3dedbf9101c18ef0511a76696ef23facb2e22a2b056b3316411ff2a9507897e9`  
		Last Modified: Thu, 31 Aug 2023 20:47:02 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed749c3c22b571714d657de1b3a348f494fcc6459ab7a50ed5d8fb34fe5c21c`  
		Last Modified: Thu, 31 Aug 2023 20:47:02 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ada0210fb91f52c20f0789a3ce47d2f2a627664645eb466d46c0aa9f346d92`  
		Last Modified: Thu, 31 Aug 2023 20:47:02 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0dd905dd5cd5c65ac0dc42c849c3c1de62136c0738109afbe00785b705d6d1b`  
		Last Modified: Thu, 31 Aug 2023 20:47:00 GMT  
		Size: 78.8 KB (78785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776fc1e472ae712a111ecdddea993bee8b9494ff603c8d916949a054597066b1`  
		Last Modified: Thu, 31 Aug 2023 20:47:00 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d789d994799e0ef2623b430ead2f296feb41b24714a30232d48933534d6523b9`  
		Last Modified: Thu, 31 Aug 2023 20:47:19 GMT  
		Size: 185.7 MB (185726755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e1be94fcc592f5216ad38694b172032e8eb04083eb324f48c0bb5dc486c19e`  
		Last Modified: Thu, 31 Aug 2023 20:47:00 GMT  
		Size: 60.9 KB (60948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6edd26ab752779156c15b9f57fd1769989f5abc1bfb0ed86b480ce8e2f620ce`  
		Last Modified: Thu, 31 Aug 2023 20:47:00 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
