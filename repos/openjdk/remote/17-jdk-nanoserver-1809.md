## `openjdk:17-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:9c3c9dafdfc3bd3ffa3a1f8a41c97902108e9093897887f71c6a5603813af172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `openjdk:17-jdk-nanoserver-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull openjdk@sha256:eed8e9ea629ca43aec8052fa47f88ac69c084b94888f54f1af2dfa0f8c472cd0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288529243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358e15917e21335f3c52959bc980268dd5f3993ddaef3e4c4d1ea8c227523593`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:53:30 GMT
SHELL [cmd /s /c]
# Wed, 14 Jul 2021 03:02:56 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 14 Jul 2021 03:02:59 GMT
USER ContainerAdministrator
# Wed, 14 Jul 2021 03:03:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Jul 2021 03:03:16 GMT
USER ContainerUser
# Thu, 15 Jul 2021 22:24:31 GMT
ENV JAVA_VERSION=17-ea+31
# Thu, 15 Jul 2021 22:24:47 GMT
COPY dir:c1ce5b9c3e35898550abea8904292ba655c6b1dc5e0002544569d91a4b8455b1 in C:\openjdk-17 
# Thu, 15 Jul 2021 22:25:08 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 15 Jul 2021 22:25:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d8754fb12dd351c91bed29d92c703cddb135a78d8f056b6a3bf13a251c1d2d`  
		Last Modified: Wed, 14 Jul 2021 03:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d058f99ef2d3fe28236834e60b39712d663043177b35defac1c8acfafd3016d5`  
		Last Modified: Wed, 14 Jul 2021 03:47:37 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456549b72e3f1534b7acf6fa76038ed24ce3663d39883813dbe50372eb3986bb`  
		Last Modified: Wed, 14 Jul 2021 03:47:36 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3002766b2def22b4702b5aee99f9816819823d022a6adab4d7e1e1aab42f9a16`  
		Last Modified: Wed, 14 Jul 2021 03:47:36 GMT  
		Size: 66.8 KB (66818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3f23d871bb0957ed5203be3aa3cf5c809b42e159fb728ed9b411dc03f6af15`  
		Last Modified: Wed, 14 Jul 2021 03:47:34 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74fdadd35230e6182976b1fe191849de3ad69d26028576d888c9752037bb56d`  
		Last Modified: Thu, 15 Jul 2021 22:39:04 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee021f504580293752788230c2e5f0c63f1afbf7fbf6ea426c0837ffe1cfbc5`  
		Last Modified: Thu, 15 Jul 2021 22:42:32 GMT  
		Size: 182.1 MB (182072182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fcc1bfa45cc10c61da4cd9d9514b107deb1924caf695f1c90bd625e7c1315d0`  
		Last Modified: Thu, 15 Jul 2021 22:39:08 GMT  
		Size: 3.7 MB (3657636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9a496036ca276db2a66107c052b290d44a2c35650ef9b90ff29dd27ab0151b`  
		Last Modified: Thu, 15 Jul 2021 22:39:04 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
