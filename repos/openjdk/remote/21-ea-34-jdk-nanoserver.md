## `openjdk:21-ea-34-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:0dad818631c657542c5329c1875dff6ed0ee3da3431d837b8114e4fffcaa850c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `openjdk:21-ea-34-jdk-nanoserver` - windows version 10.0.17763.4645; amd64

```console
$ docker pull openjdk@sha256:b9e6f8b9da0521d5d319252335b53c4e0a4bd27c2c3e46946eaef16f4ffb2c34
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.3 MB (306343028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c214987375a6e9a684890f5d021b23cc0bd50d54c0950d2b1207f6c229384b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Thu, 13 Jul 2023 21:36:32 GMT
SHELL [cmd /s /c]
# Fri, 14 Jul 2023 00:19:53 GMT
ENV JAVA_HOME=C:\openjdk-21
# Fri, 14 Jul 2023 00:19:53 GMT
USER ContainerAdministrator
# Fri, 14 Jul 2023 00:20:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 14 Jul 2023 00:20:02 GMT
USER ContainerUser
# Fri, 04 Aug 2023 00:22:32 GMT
ENV JAVA_VERSION=21-ea+34
# Fri, 04 Aug 2023 00:22:48 GMT
COPY dir:126ff8951f9bbf5674d101616b5f2446db8fd119962bcdeb4c41f4d89b400077 in C:\openjdk-21 
# Fri, 04 Aug 2023 00:23:01 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 04 Aug 2023 00:23:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13c473988daf5951866dd9b290bd6417227c1d7df6e811cfe11438d033a1eba`  
		Last Modified: Thu, 13 Jul 2023 22:19:06 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289ea5fc8a7f31b38120d64f4fc304a5e09ac629f99bc9b5e92a4349bcf143bf`  
		Last Modified: Fri, 14 Jul 2023 00:25:00 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66b7bdcadf86bdda397cf414ae45f974a40e697d5002156e00e7cd59e946cbc`  
		Last Modified: Fri, 14 Jul 2023 00:25:00 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d929e2c9bf4cff0381fd000609dc5a373e8d51ceaca78fe43f609176c7d62d78`  
		Last Modified: Fri, 14 Jul 2023 00:25:00 GMT  
		Size: 67.7 KB (67668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ab158d7279412c8630521a444777102ad52479439f793e296ac44ef396e701`  
		Last Modified: Fri, 14 Jul 2023 00:24:58 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7294dbed7ee48a4e50cd9347a713c05b84ea7f7ff41d7bbf6084b93ee9e84f`  
		Last Modified: Fri, 04 Aug 2023 00:27:42 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c013b248d10d79433b71a20e75d21c41424ea1443589e6a4646f3720f9c40a`  
		Last Modified: Fri, 04 Aug 2023 00:28:03 GMT  
		Size: 198.0 MB (198037077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d53da186bc8a9eedba019f6d2f66c8479369c5377e8cf6f0b20306cb9db7a37`  
		Last Modified: Fri, 04 Aug 2023 00:27:43 GMT  
		Size: 3.8 MB (3823100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c500dbd8d5e4cdc5a0b3b33293bec8d6d839ecfd435629a51118324d3de5021f`  
		Last Modified: Fri, 04 Aug 2023 00:27:42 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
