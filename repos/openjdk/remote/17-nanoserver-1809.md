## `openjdk:17-nanoserver-1809`

```console
$ docker pull openjdk@sha256:788c2f3d664ec80eef9fbd2bb8b59aaa287aa41f862ea4e7607f5bf1646a2bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `openjdk:17-nanoserver-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull openjdk@sha256:e4cf34bc34c4ab773cf2d739933fbcd112152d238bd3c8163256547083cf8e60
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288524842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a034233d0a48ff700841c53792d4a859b6406a242a7d2846e6c227e72adcb4`
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
# Fri, 30 Jul 2021 19:23:32 GMT
ENV JAVA_VERSION=17-ea+33
# Fri, 30 Jul 2021 19:23:49 GMT
COPY dir:c2f847368e66ae5d1c1768e6a61e34d3d64fde6eba881c5b8063643b3194b094 in C:\openjdk-17 
# Fri, 30 Jul 2021 19:24:11 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 30 Jul 2021 19:24:13 GMT
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
	-	`sha256:31735615c60762c1e25bb5c3a42ce71e24c6b5ac8301dbcb3d41060d907f9e69`  
		Last Modified: Fri, 30 Jul 2021 19:35:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ac7f940b629cf36f62937e4fdeff7acafab6fdd62dcc7c3a2a19bcdbdbf445`  
		Last Modified: Fri, 30 Jul 2021 19:38:56 GMT  
		Size: 182.1 MB (182079785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258da2047ba45e0305c758c85bc89544f0fa71567762788d01ebf1e39b973d6b`  
		Last Modified: Fri, 30 Jul 2021 19:35:41 GMT  
		Size: 3.6 MB (3645749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c4de7fc728b7a8be7901b36e55c83f1792c16faba825ed74f68aaf3868114c`  
		Last Modified: Fri, 30 Jul 2021 19:35:37 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
