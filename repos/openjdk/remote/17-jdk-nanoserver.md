## `openjdk:17-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:49cc24e7b9d52a58a5c0512092fbee2dfd96c55f28a24ec45c185db2bbbb8ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `openjdk:17-jdk-nanoserver` - windows version 10.0.17763.2061; amd64

```console
$ docker pull openjdk@sha256:258c64b378176e585ec3b2aa7a2fe989a759c654245e6d2362b78c885dbc4c4f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288514883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba25b4ae1b9ca3fe0ff0e317e352f26ac78142b7af817fc894fc765a8eec562`
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
# Fri, 23 Jul 2021 18:37:16 GMT
ENV JAVA_VERSION=17-ea+32
# Fri, 23 Jul 2021 18:37:34 GMT
COPY dir:c4d9a1019d03f0b9e7248012a1b46ae8d59273f95357c30673f022357ad456ad in C:\openjdk-17 
# Fri, 23 Jul 2021 18:38:07 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 23 Jul 2021 18:38:09 GMT
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
	-	`sha256:7bae324ffe7b007c1928a4f26568fa1c6efdffabc6e86348595513f885a89d8f`  
		Last Modified: Fri, 23 Jul 2021 18:50:19 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3487519511a31888655c2c3382a124ba139ec745f0025d3cb27de95584f596c`  
		Last Modified: Fri, 23 Jul 2021 18:50:38 GMT  
		Size: 182.1 MB (182070449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8c03a8f063b69aa15e3ebf91550d5e2c861854fd76cc3d304ee8042880a04a`  
		Last Modified: Fri, 23 Jul 2021 18:50:20 GMT  
		Size: 3.6 MB (3645042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c735f330dbe29826553f0e15d0778e116edc2737f94e7935297df1411d0b8d3`  
		Last Modified: Fri, 23 Jul 2021 18:50:19 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
