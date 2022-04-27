## `eclipse-temurin:11-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:1654061754b51ba860884270992b69eb29913f74a9e31dcf6d5caf2438142fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.643; amd64
	-	windows version 10.0.17763.2803; amd64

### `eclipse-temurin:11-nanoserver` - windows version 10.0.20348.643; amd64

```console
$ docker pull eclipse-temurin@sha256:d83e141cf8b16b115c76dcef313e804d5f9bd85aa9b2bcc5960fdf93491992bc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.0 MB (309980703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231dab386e723ff7f6ec5ee1ce5551c83f2c2b7d4cbf194f97c481f7b95611f1`
-	Default Command: `["jshell"]`
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
# Wed, 27 Apr 2022 18:38:00 GMT
COPY dir:1583ce76f01a2d0a0742f7b70646c210ef8c619565a381c37e5a1156f6ec4636 in C:\openjdk-11 
# Wed, 27 Apr 2022 18:38:13 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 27 Apr 2022 18:38:14 GMT
CMD ["jshell"]
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
	-	`sha256:be053a27093aaee8ab0326357bbd3d9a296d10105b82d8140b988cc3b3d0120d`  
		Last Modified: Wed, 27 Apr 2022 19:58:03 GMT  
		Size: 192.2 MB (192225276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97e45eaf7db593d039300f46a54a9fd5d2b3c116cb3a16c1c89c98fdbb85a86`  
		Last Modified: Wed, 27 Apr 2022 19:54:28 GMT  
		Size: 70.6 KB (70627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b9db188b5620905557c35ea59efbc7cce9049f06187906f62414aafbe1a8ab`  
		Last Modified: Wed, 27 Apr 2022 19:54:28 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-nanoserver` - windows version 10.0.17763.2803; amd64

```console
$ docker pull eclipse-temurin@sha256:d203e5a7feba27a2f8d68430af69616dcfc793555a763b9db0ce108498f7096f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295461565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda2c1fd64398159eab84e7cd5a70c576d4ba7a617170d737b4a010e94feef5b`
-	Default Command: `["jshell"]`
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
# Wed, 27 Apr 2022 18:21:40 GMT
COPY dir:1583ce76f01a2d0a0742f7b70646c210ef8c619565a381c37e5a1156f6ec4636 in C:\openjdk-11 
# Wed, 27 Apr 2022 18:21:52 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 27 Apr 2022 18:21:53 GMT
CMD ["jshell"]
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
	-	`sha256:8e24cc56a925d9d31eddc10025b2407bf8c983538af989673986520512b9980e`  
		Last Modified: Wed, 27 Apr 2022 19:38:09 GMT  
		Size: 192.2 MB (192228060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529190f8c9a68f1c9e9b26612e5668547b1f4e63b79a7627c00afef0d73c959d`  
		Last Modified: Wed, 27 Apr 2022 19:34:37 GMT  
		Size: 59.9 KB (59908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3760337640a37a575b4e060afd8fe49aac4b213855fbd3e58ad1f46c1fc2969`  
		Last Modified: Wed, 27 Apr 2022 19:34:37 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
