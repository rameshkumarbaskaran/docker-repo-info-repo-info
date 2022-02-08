## `openjdk:18-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:90a25b600a66f778c56736ce853ee2bcd5c94840a935fd411a74a69bb183a9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `openjdk:18-jdk-nanoserver-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull openjdk@sha256:cc78ee65ab4e7c5da1168d2fdd7eed9f01235cd9e7fb5898928d23324a702b43
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.7 MB (290693715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cafab91aa57515bf1828d4f502885450858a605da0b2b66d1c12276c1d0d2162`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 19 Jan 2022 22:25:45 GMT
SHELL [cmd /s /c]
# Wed, 19 Jan 2022 22:28:51 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 19 Jan 2022 22:28:52 GMT
USER ContainerAdministrator
# Wed, 19 Jan 2022 22:29:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 19 Jan 2022 22:29:07 GMT
USER ContainerUser
# Tue, 08 Feb 2022 02:24:57 GMT
ENV JAVA_VERSION=18-ea+34
# Tue, 08 Feb 2022 02:25:29 GMT
COPY dir:570e617dc3556cc51d89cab6828d06005ee18874ddb9f3b36631503cd07a7d0d in C:\openjdk-18 
# Tue, 08 Feb 2022 02:25:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 08 Feb 2022 02:25:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a1b3e13bb7b3d4b61b5f49a91d6eb9bfcf5539ab89c3687d608f17713c2409b5`  
		Last Modified: Thu, 20 Jan 2022 02:21:30 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848f0583ef29156642246562456f8e070e665d934ee5b5eca5da3a549c83b769`  
		Last Modified: Thu, 20 Jan 2022 02:26:27 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e408e60a5374b05b851d28c9154c5da23c66b31ff9344a9d4aa29e471f89a90f`  
		Last Modified: Thu, 20 Jan 2022 02:26:27 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fd9cc1e1a14cc04328a97d502fe56af7c5256437bad3c9c13e77832c28f28e`  
		Last Modified: Thu, 20 Jan 2022 02:26:27 GMT  
		Size: 68.6 KB (68587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cd88d42425b3a9d8b74a22ca8c7ca9daaa1903b0a06ee4fd2194cd5acf6362`  
		Last Modified: Thu, 20 Jan 2022 02:26:25 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed014fe2f91a4c801eccfb11928313e627232322438747616504a406962db9a`  
		Last Modified: Tue, 08 Feb 2022 03:39:18 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4124d747a5e565c3c22f213739462ec453b2633e25c0ac93a89548cf10f9742b`  
		Last Modified: Tue, 08 Feb 2022 03:42:31 GMT  
		Size: 184.0 MB (183988419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6856e48fb39b154147dae4ca1ec28870f4c16352acbd936195d5a8b42b909fe8`  
		Last Modified: Tue, 08 Feb 2022 03:39:19 GMT  
		Size: 3.6 MB (3583296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bf3c0407ccc8bda0643a4c9fdc1ca409bad96c9f06d93b2f21bde85be49f03`  
		Last Modified: Tue, 08 Feb 2022 03:39:18 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
