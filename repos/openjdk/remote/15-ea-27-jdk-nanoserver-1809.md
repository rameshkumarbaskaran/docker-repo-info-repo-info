## `openjdk:15-ea-27-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:45ee5d764f044af36fa71c2f1ab458c786fef18f221f8d5536033423851910df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `openjdk:15-ea-27-jdk-nanoserver-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull openjdk@sha256:4ea33c983c15f0cd30678990fc043be2f7b662a4679165ac51df5f4e022c578e
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295908234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa0a0040d7fc1321a86be30077cf3b176ebe19203111ac12c903160330ea5d6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jun 2020 11:12:32 GMT
RUN Apply image 1809-amd64
# Tue, 09 Jun 2020 22:42:44 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2020 22:42:45 GMT
ENV JAVA_HOME=C:\openjdk-15
# Tue, 09 Jun 2020 22:42:45 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2020 22:43:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Tue, 09 Jun 2020 22:43:01 GMT
USER ContainerUser
# Mon, 15 Jun 2020 21:56:53 GMT
ENV JAVA_VERSION=15-ea+27
# Mon, 15 Jun 2020 21:57:39 GMT
COPY dir:fc30e1260816c1b88213b82122404465922112b39d06f14c63c612c23834f328 in C:\openjdk-15 
# Mon, 15 Jun 2020 21:58:11 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Mon, 15 Jun 2020 21:58:12 GMT
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
	-	`sha256:66a124a49383ae5eb05208979bcfbadf68055d2672da7f78201fe9a45e8d0bbb`  
		Last Modified: Tue, 09 Jun 2020 23:19:14 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb0c11b8fc0c6457077b02c8314626c0346af177c44a8615448f933e94b909c`  
		Last Modified: Tue, 09 Jun 2020 23:19:13 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29f17e75290909d8f60805f97895317f25ce6c2dc53b1b25e8d6dfe142e6f53`  
		Last Modified: Tue, 09 Jun 2020 23:19:13 GMT  
		Size: 63.5 KB (63500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fe65db6982f49c866229851adc1c64f6e6354b9e0a49d506241693ac2e660f`  
		Last Modified: Tue, 09 Jun 2020 23:19:11 GMT  
		Size: 814.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e942b66f8e8cff229cb7f8775caa79fb5bb8186d4d80dc5837ec7ab9f77a6d69`  
		Last Modified: Mon, 15 Jun 2020 22:03:27 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185d76d03b1ff8864eaf32ef3a9403d6ee756c653d6b114568709404bd3e5921`  
		Last Modified: Mon, 15 Jun 2020 22:03:49 GMT  
		Size: 191.3 MB (191264860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d35b60126276e420d40587d42ac07eb79cffc9b67d76e4ba7ba62dfe47ef11`  
		Last Modified: Mon, 15 Jun 2020 22:03:30 GMT  
		Size: 3.5 MB (3531321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b442a795765f79371b07e8aa4a593d9e4b984e5a0b61be1042c4b10a68ffa1`  
		Last Modified: Mon, 15 Jun 2020 22:03:28 GMT  
		Size: 928.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
