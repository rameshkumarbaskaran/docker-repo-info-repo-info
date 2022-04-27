## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:d78aaae32826912ce20cef8c4a3346e9007484b4b1b93092c6b933a7cb8ebe6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.643; amd64
	-	windows version 10.0.17763.2803; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.643; amd64

```console
$ docker pull eclipse-temurin@sha256:83f420d901bcda5edc1cbca7ab7ea47e881316466c8d40df846220d4d50fe79b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160543434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b9681d48e207d6d5ae9ee147ff988109fbaf38e88fd58363952c535b282f2f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 03 Apr 2022 05:29:07 GMT
RUN Apply image ltsc2022-amd64
# Wed, 13 Apr 2022 15:47:59 GMT
SHELL [cmd /s /c]
# Wed, 27 Apr 2022 18:37:36 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Wed, 27 Apr 2022 18:37:36 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 27 Apr 2022 18:37:37 GMT
USER ContainerAdministrator
# Wed, 27 Apr 2022 18:37:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 27 Apr 2022 18:37:46 GMT
USER ContainerUser
# Wed, 27 Apr 2022 18:38:28 GMT
COPY dir:b81e8d840693600453cb21437c037772b6cbe813879626cf7da1b40ae8a26737 in C:\openjdk-11 
# Wed, 27 Apr 2022 18:38:38 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5ee98801bdad72bc36678d072c89f7dd482fee29086c1d9c8ad6ff0cb5afa385`  
		Size: 117.6 MB (117579416 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:924a7c42e559a85c0bc74dbb028ddeee43fe67b0f59c81c60cbda0082e0e3ae5`  
		Last Modified: Wed, 13 Apr 2022 16:38:31 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3224a198810aab7f19aa11b517e82096b417f1d6500e979c6e0e6e45528fb0`  
		Last Modified: Wed, 27 Apr 2022 19:54:30 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fd0da3fe01b581fd0e3f01ec7526855a29f8b5bd5b1b58bf6999cb80fe2ec2`  
		Last Modified: Wed, 27 Apr 2022 19:54:30 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2450f7d386cea4b51ca60429eb1ce4e3445d3a58c2921cd28d7a34151c20a2cf`  
		Last Modified: Wed, 27 Apr 2022 19:54:30 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d1a6ce74676ceb12c83212ee6bd8b3b31b1325906ea6875940559173535c9e`  
		Last Modified: Wed, 27 Apr 2022 19:54:28 GMT  
		Size: 98.5 KB (98534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a962d5931d7db5304b9c7d90fb60f863b14cc2327d2bc9535ba1731ed479087`  
		Last Modified: Wed, 27 Apr 2022 19:54:28 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a012295a1c5f1f9522242b5082e55cc915d2be7b6c62d81081faf0a2f8a0706`  
		Last Modified: Wed, 27 Apr 2022 19:59:03 GMT  
		Size: 42.8 MB (42791106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74776169f748e8524c7c537223549c6500293cf73e92ded224f04f35fa9ab601`  
		Last Modified: Wed, 27 Apr 2022 19:58:17 GMT  
		Size: 68.7 KB (68692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.2803; amd64

```console
$ docker pull eclipse-temurin@sha256:8b61676df2c6c511725ad4ae882a89942ba75ee3c8d390e47c38fb5eff34ed8c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (146038384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed1aab1d4c076763ac6316e12abdf22eae6f843e1d56d0c2357597502f6cd55`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 15:16:11 GMT
SHELL [cmd /s /c]
# Wed, 27 Apr 2022 18:21:15 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Wed, 27 Apr 2022 18:21:16 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 27 Apr 2022 18:21:17 GMT
USER ContainerAdministrator
# Wed, 27 Apr 2022 18:21:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 27 Apr 2022 18:21:26 GMT
USER ContainerUser
# Wed, 27 Apr 2022 18:26:18 GMT
COPY dir:b81e8d840693600453cb21437c037772b6cbe813879626cf7da1b40ae8a26737 in C:\openjdk-11 
# Wed, 27 Apr 2022 18:26:29 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ea4009814dceb50337c66614a6008cfc2fb73ce53e62162bce071ef6ea1adf2d`  
		Last Modified: Wed, 13 Apr 2022 15:58:06 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85237bed8ad6af9a5e13adcc58acf32b17e256daee93388dbeb99587a6c3f81c`  
		Last Modified: Wed, 27 Apr 2022 19:34:39 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20ba0a2dd0ae4ff85fd6bda92809f711c0e787862b2b73f99d122fbe7571d04`  
		Last Modified: Wed, 27 Apr 2022 19:34:40 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02adef8566426a37333c572ab4825cee0f524fb88464726ff0aca5af1edd6066`  
		Last Modified: Wed, 27 Apr 2022 19:34:39 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1e29ba11320baa821bac59fa33f9f49bc24430626872a323f3da170859d9f6`  
		Last Modified: Wed, 27 Apr 2022 19:34:37 GMT  
		Size: 70.6 KB (70584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c23db479c6832cc4cdb3b025e96bf121b09f618a34225523b692e4b8ffd466e`  
		Last Modified: Wed, 27 Apr 2022 19:34:37 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58388047dbe1e443f616687a812fcf95125ce5258a7118bf8ba8df53fbaa88ce`  
		Last Modified: Wed, 27 Apr 2022 19:42:07 GMT  
		Size: 42.8 MB (42807285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6480be98ab4a3f328f050d6c5d5ed0d609013546906bb54fe34123b90b3b817b`  
		Last Modified: Wed, 27 Apr 2022 19:41:21 GMT  
		Size: 58.7 KB (58662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
