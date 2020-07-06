## `openjdk:16-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:a2a4c7c46268603e3c6d2d26b10ee85d27c64a630e5c2a982d8bb1e6755d58f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `openjdk:16-jdk-nanoserver` - windows version 10.0.17763.1282; amd64

```console
$ docker pull openjdk@sha256:8759b446141d2e649e74236bfa9a36e092039dea14335dd30fa7bff1fbbf1c00
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (296011219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417001130aa86ca64552c5d9648d54a77b11b99a93504023712b1f2f99f6cdf9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jun 2020 11:12:32 GMT
RUN Apply image 1809-amd64
# Tue, 09 Jun 2020 22:42:44 GMT
SHELL [cmd /s /c]
# Thu, 18 Jun 2020 21:20:54 GMT
ENV JAVA_HOME=C:\openjdk-16
# Thu, 18 Jun 2020 21:20:55 GMT
USER ContainerAdministrator
# Thu, 18 Jun 2020 21:21:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Thu, 18 Jun 2020 21:21:11 GMT
USER ContainerUser
# Mon, 06 Jul 2020 20:21:36 GMT
ENV JAVA_VERSION=16-ea+4
# Mon, 06 Jul 2020 20:22:20 GMT
COPY dir:12187a50a00bae270e2ec62fbb2164e71b4cde754d915f2538c3e37c1c5dcf62 in C:\openjdk-16 
# Mon, 06 Jul 2020 20:22:51 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Mon, 06 Jul 2020 20:22:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c7d6d47ff7dfb2aa4d4e819641b93ec971e8541978dff0ffc24c193babeb8c07`  
		Size: 101.0 MB (101043386 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5b390ee94e41353252b153770fa99d748992b90bdaf9abf7c785d93be52ee02c`  
		Last Modified: Tue, 09 Jun 2020 23:19:14 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6735890902f0d30df68ef896ea73cd7d60bdd05747cff4957193c1e609fff89a`  
		Last Modified: Thu, 18 Jun 2020 21:28:21 GMT  
		Size: 864.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee48b3407ba988368d7894a7733194fa4aa014b7f58f2d8c7fcaef8e2671a28`  
		Last Modified: Thu, 18 Jun 2020 21:28:21 GMT  
		Size: 876.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6045b891a8218b59a2fddf2b6cac14838a3415c9d2d3092bc26b5e034902d9a`  
		Last Modified: Thu, 18 Jun 2020 21:28:21 GMT  
		Size: 67.2 KB (67242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f442edf533cb5c66c3872015a3894f657674d730051b398dd331afcfe90617`  
		Last Modified: Thu, 18 Jun 2020 21:28:18 GMT  
		Size: 910.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8562cba2b567de4884a57673cbb26a7ccf563a205ed3a3e42bbeaba4218e1ae3`  
		Last Modified: Mon, 06 Jul 2020 21:05:18 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe0abcfa23b43dbcac996a9ff9af976bb64897f6f314d2c55adb3a5efed81af`  
		Last Modified: Mon, 06 Jul 2020 21:05:42 GMT  
		Size: 191.4 MB (191419978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fddaeea3d573c045e29e1cd51a26e93868abfb03a8028ccc291c268246e5dc68`  
		Last Modified: Mon, 06 Jul 2020 21:05:19 GMT  
		Size: 3.5 MB (3475329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d00747dab19e76dce4f22f01cdfa5f2d2adc5f3d918b343ad196d27d51629cf`  
		Last Modified: Mon, 06 Jul 2020 21:05:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
