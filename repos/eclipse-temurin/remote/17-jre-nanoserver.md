## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:282030795886766f51daff6926ce4bd8ba830aae35e1a3a4aaf8bb0f308dfef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1906; amd64
	-	windows version 10.0.17763.4737; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.1906; amd64

```console
$ docker pull eclipse-temurin@sha256:b0851e4cca37591022062fcdd619e2f687af97914910fb2a657d7a698cf03177
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164049249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af2864c1593f70a035c37102d50a0445da09b48a7582e2f553b25054ef1b4f7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Thu, 31 Aug 2023 20:37:45 GMT
COPY dir:a0385e93ace109911eb3f9b447c778bc50121e83afa8a78ec38a5f32b2b463cb in C:\openjdk-17 
# Thu, 31 Aug 2023 20:37:57 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:739243e7e5216693eeca717e6987aeafecc147eabb4181b76ab7fd40b0e22e0b`  
		Last Modified: Thu, 31 Aug 2023 20:47:39 GMT  
		Size: 43.4 MB (43403478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55676300f30ab4cc690673c5459eaf342c63b1c406678df0fcecbbd1102ce452`  
		Last Modified: Thu, 31 Aug 2023 20:47:31 GMT  
		Size: 61.0 KB (60974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.4737; amd64

```console
$ docker pull eclipse-temurin@sha256:6249d8b430a88ceb4825bd6f4eb3ec315ed5ca91de01c16a7587312c0d595df3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150978417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2ea1f86bf46b85b51d27e4a6af1bbcea58485eff2e4523a5b64e5daa3c4bee`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Aug 2023 08:33:47 GMT
RUN Apply image 10.0.17763.4737
# Wed, 09 Aug 2023 23:39:50 GMT
SHELL [cmd /s /c]
# Thu, 31 Aug 2023 20:29:57 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Thu, 31 Aug 2023 20:29:57 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 31 Aug 2023 20:29:58 GMT
USER ContainerAdministrator
# Thu, 31 Aug 2023 20:30:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 31 Aug 2023 20:30:08 GMT
USER ContainerUser
# Thu, 31 Aug 2023 20:34:19 GMT
COPY dir:a0385e93ace109911eb3f9b447c778bc50121e83afa8a78ec38a5f32b2b463cb in C:\openjdk-17 
# Thu, 31 Aug 2023 20:34:31 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:86fab75eb466cadf89d853682179b3b57eba9fe28c78041dd52bced81e18a627`  
		Last Modified: Tue, 08 Aug 2023 17:55:54 GMT  
		Size: 104.5 MB (104459386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7e08c5247c8c7d832882da17ac85015e9dd4d4dfc9e4114fc14746eb2abded`  
		Last Modified: Thu, 10 Aug 2023 00:21:01 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d579180f9e61898dea123c9b4c0edc42b464dfd0f1a7bc133ba5655d2e278339`  
		Last Modified: Thu, 31 Aug 2023 20:44:38 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d8d37e7bf677fa0f1e142ce3a584705d3dcedb61165384f14e741d85d54e3b`  
		Last Modified: Thu, 31 Aug 2023 20:44:38 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d18db2a934997819fa0aea584565d61b3eb49a1659fd37162c3f505085a63c`  
		Last Modified: Thu, 31 Aug 2023 20:44:38 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cf24a0a592732136360d0e90f43927b9a1838ff4cf624f7fbb41f749cce2fe`  
		Last Modified: Thu, 31 Aug 2023 20:44:36 GMT  
		Size: 68.4 KB (68399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e493056b4915706cebf68bed038b953c19967daae6657b4d89a828bc9cea09`  
		Last Modified: Thu, 31 Aug 2023 20:44:36 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6881ec53c717f43566c7efc0ad6bcc0b68710b2abe2bf8fb843df59f11b1f93`  
		Last Modified: Thu, 31 Aug 2023 20:45:56 GMT  
		Size: 43.4 MB (43403276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9c80b527058fa4acb06567e780146065fd9d1a67ca2e2367b2e739c587613b`  
		Last Modified: Thu, 31 Aug 2023 20:45:48 GMT  
		Size: 3.0 MB (3041978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
