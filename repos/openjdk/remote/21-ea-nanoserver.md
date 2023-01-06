## `openjdk:21-ea-nanoserver`

```console
$ docker pull openjdk@sha256:902173f9942dfd32fa1f26575edce0ea6b3bb8891384b210357d246b4f88bd50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `openjdk:21-ea-nanoserver` - windows version 10.0.17763.3770; amd64

```console
$ docker pull openjdk@sha256:6e2ffa08d485829dafff1535bb975f439905b768f0d14f037c92f137a8c6d498
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.5 MB (304461640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2784d588c1ab094146ad3421c444b66ad67afa76435d50e79d104056266d1200`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Tue, 13 Dec 2022 22:53:34 GMT
SHELL [cmd /s /c]
# Wed, 14 Dec 2022 02:56:32 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 14 Dec 2022 02:56:33 GMT
USER ContainerAdministrator
# Wed, 14 Dec 2022 02:57:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Dec 2022 02:57:30 GMT
USER ContainerUser
# Fri, 06 Jan 2023 19:25:23 GMT
ENV JAVA_VERSION=21-ea+4
# Fri, 06 Jan 2023 19:25:39 GMT
COPY dir:98c725faeffa1c17989d4d626b6c9a2efc8eb8cb88209a3ce78e144bc2abc6d1 in C:\openjdk-21 
# Fri, 06 Jan 2023 19:26:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 06 Jan 2023 19:26:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fe06cbef5ac46e54edd743daf1bc2bfa36b294c7ce9104837061c41a4bde7b`  
		Last Modified: Tue, 13 Dec 2022 23:57:01 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f403eb4656dcd257924d61f24cde07e6a0bd4ea52ceb2fbb6aabbe94c2b76b67`  
		Last Modified: Wed, 14 Dec 2022 08:47:11 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfa39493326e86ec6b2f2fd8125ad183b1ed64b2c3f2a4461f05d827cc0926a`  
		Last Modified: Wed, 14 Dec 2022 08:47:11 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b7523c236c3ef82ccdd5905f89f123933015a7d581e70a248676aa7e3a76df`  
		Last Modified: Wed, 14 Dec 2022 08:47:11 GMT  
		Size: 66.3 KB (66297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063f4c761ac43a960d04eea23db92193fd5460a992bd8ac71186731abb9de13c`  
		Last Modified: Wed, 14 Dec 2022 08:47:09 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1170fa6f681c5e336b989cbd327a32dbbc0f4009726a0dce1a646913e29de60c`  
		Last Modified: Fri, 06 Jan 2023 20:19:53 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe14d819c2501cba598cd8ddfd46f3e27d65845eb8e3b7834655371b37c8029a`  
		Last Modified: Fri, 06 Jan 2023 20:20:16 GMT  
		Size: 194.0 MB (193953497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ceedafd5f1416c4fc6edada5895a2b17d3e72399df2af0d94eae256bc306e95`  
		Last Modified: Fri, 06 Jan 2023 20:19:55 GMT  
		Size: 3.8 MB (3763890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65072676600df52881e4421cd7fc86cd94cb7381c4af4d878ab4a3e16cda784f`  
		Last Modified: Fri, 06 Jan 2023 20:19:53 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
