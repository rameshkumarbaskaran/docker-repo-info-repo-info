## `openjdk:16-ea-30-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:ee4c90024ea5d84c5cd84db44926b44b9998fa6c4f42fa98130b0b06d6bbabb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `openjdk:16-ea-30-jdk-nanoserver` - windows version 10.0.17763.1637; amd64

```console
$ docker pull openjdk@sha256:6f4638cd274018e2e1e12321b8ee8b1b257abd7066015ce6c43f59f2084ae106
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285137181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d2e445f9f2a068537f0756737df9bf772d4b33d493b3f53630be2806975a17`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 18:58:23 GMT
SHELL [cmd /s /c]
# Wed, 09 Dec 2020 18:58:23 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 09 Dec 2020 18:58:24 GMT
USER ContainerAdministrator
# Wed, 09 Dec 2020 18:58:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 09 Dec 2020 18:58:40 GMT
USER ContainerUser
# Mon, 28 Dec 2020 18:19:57 GMT
ENV JAVA_VERSION=16-ea+30
# Mon, 28 Dec 2020 18:20:34 GMT
COPY dir:b6d103ebd9e56fa7bbf1c241ffdf905dc15fa27c9064bbcf3e6b5acc32320afc in C:\openjdk-16 
# Mon, 28 Dec 2020 18:20:56 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Mon, 28 Dec 2020 18:20:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fe9a51a0164bd1c063cbda08c4e22dc4f5d04a8047a3951d7441f37fb93c57f2`  
		Last Modified: Wed, 09 Dec 2020 19:34:04 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8993beeae33a05d68775319a4b9f9df44ac08ccfc62cb15113a36b06ad62d1f`  
		Last Modified: Wed, 09 Dec 2020 19:34:02 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340da9582f81cba4147b5da6d500dacd9f3ffdd520c3211dfb20153cd4ae71fc`  
		Last Modified: Wed, 09 Dec 2020 19:34:02 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f848f35781549a8c193011c95049cd95311b558af39d0f8057a5b460a459488`  
		Last Modified: Wed, 09 Dec 2020 19:34:02 GMT  
		Size: 64.6 KB (64579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636f94045101715dca150f5013879c45929dec9e849eac5b53631727e42bb8a6`  
		Last Modified: Wed, 09 Dec 2020 19:33:59 GMT  
		Size: 873.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e24b11c3220d71175412241ac97f0f93e00c9ef1df9082e9bd1eb1e7cdc75f8`  
		Last Modified: Mon, 28 Dec 2020 18:27:26 GMT  
		Size: 832.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ee32a8974199121113474d1b02ec63ea580b93694cf95ef70cd6d024f925dc`  
		Last Modified: Mon, 28 Dec 2020 18:27:45 GMT  
		Size: 180.1 MB (180116633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beaaf8b29e0f1ccefbd6f46bb7766ba2b55824aa5e855bdfec88d5cd8d187bf6`  
		Last Modified: Mon, 28 Dec 2020 18:27:28 GMT  
		Size: 3.7 MB (3686002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a30d269e7a2119d8171158b250e9a182a13087ec370336fef5dd4923fdec4f`  
		Last Modified: Mon, 28 Dec 2020 18:27:27 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
