## `openjdk:19-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:8415f265022efbfa90ee23b0b9aab13eeae333d8363162ad471edeec5109c754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `openjdk:19-jdk-nanoserver-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull openjdk@sha256:b3283a0139ac0136b9da588e5894e4f03d6dd546f451aafb7a32f0fff950b397
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291542595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0bad524d5728929eeca642c914c900528f6fe0261616636b79a5608bd36b6a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 19 Jan 2022 22:25:45 GMT
SHELL [cmd /s /c]
# Wed, 19 Jan 2022 22:25:45 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 19 Jan 2022 22:25:46 GMT
USER ContainerAdministrator
# Wed, 19 Jan 2022 22:25:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 19 Jan 2022 22:26:00 GMT
USER ContainerUser
# Wed, 19 Jan 2022 22:26:00 GMT
ENV JAVA_VERSION=19-ea+5
# Wed, 19 Jan 2022 22:26:30 GMT
COPY dir:c89ee721105ed55c7d82b0dd558c2f6e96bfc580298e900e2ae1409e8cfd62eb in C:\openjdk-19 
# Wed, 19 Jan 2022 22:26:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 19 Jan 2022 22:26:45 GMT
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
	-	`sha256:d37e2d9d248af5cc77da02f6689e73057a6b209b1e2cc18d237e2225251d508c`  
		Last Modified: Thu, 20 Jan 2022 02:21:30 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a757e837e961d995033dd26e4129e5adf88e7675118d83eb95cfccdd2f5170`  
		Last Modified: Thu, 20 Jan 2022 02:21:30 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8711fe31967a4951c1345f1b126afe50ed968967c304e43d8e05224db1186e7f`  
		Last Modified: Thu, 20 Jan 2022 02:21:29 GMT  
		Size: 72.5 KB (72539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0481682eb573fcc3023c5291f96696ee373749cac12ceec16c1f2a990b142e78`  
		Last Modified: Thu, 20 Jan 2022 02:21:27 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20866288a940204fd7f341fcbf4394935910cde5e050446469925f92f4b37049`  
		Last Modified: Thu, 20 Jan 2022 02:21:27 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e378d8d6b080c07fa471b885ae7a10967dfdc1f3261c40021bce2319d8f6985`  
		Last Modified: Thu, 20 Jan 2022 02:21:48 GMT  
		Size: 184.9 MB (184902286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b4eb6267866a5e3aff042451073fc5b1fe64e92ed2b1e50645f63ae7fd7d57`  
		Last Modified: Thu, 20 Jan 2022 02:21:28 GMT  
		Size: 3.5 MB (3514280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62b10098dddc1041fb637b9365b0c37e7e40afe239e8ccf6bc5d8f683557499`  
		Last Modified: Thu, 20 Jan 2022 02:21:27 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
