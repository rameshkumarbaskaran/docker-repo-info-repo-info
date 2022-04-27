## `eclipse-temurin:11-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:97aec63679abd3dec083414d35d730a6f514b7adf165cd321cc0abf3338482ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `eclipse-temurin:11-nanoserver-1809` - windows version 10.0.17763.2803; amd64

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
