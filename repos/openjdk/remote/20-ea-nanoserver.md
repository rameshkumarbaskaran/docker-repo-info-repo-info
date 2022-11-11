## `openjdk:20-ea-nanoserver`

```console
$ docker pull openjdk@sha256:9b1ac96dcd09a6882c1333fff9597bc6cf9388056837ae23fc6ff888cf03d886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `openjdk:20-ea-nanoserver` - windows version 10.0.17763.3650; amd64

```console
$ docker pull openjdk@sha256:2f15ff9836abf26d7660c50bc6310b7a23e45aaba291b31cfe0ed5076cea556c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303752076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7db5f57acc3a4ba2c07476fc987c405fd12c6f5313c92715a9f51e466825cec`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Tue, 08 Nov 2022 18:36:25 GMT
SHELL [cmd /s /c]
# Wed, 09 Nov 2022 17:26:48 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 09 Nov 2022 17:26:49 GMT
USER ContainerAdministrator
# Wed, 09 Nov 2022 17:27:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Nov 2022 17:27:07 GMT
USER ContainerUser
# Thu, 10 Nov 2022 22:20:10 GMT
ENV JAVA_VERSION=20-ea+23
# Thu, 10 Nov 2022 22:20:25 GMT
COPY dir:104a270a74e06be6306a194ecfe6148da49d7ef8d394cd7275968f9f027e2295 in C:\openjdk-20 
# Thu, 10 Nov 2022 22:20:49 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 10 Nov 2022 22:20:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e8f4bb4b79b67857c1e4ac5c66026fd5ff5badbde5a8b59b11251b02699586`  
		Last Modified: Tue, 08 Nov 2022 19:44:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5380ecadb3b5072bd5e7cf41fa446b5ae89ef7d71fde34772d7b32062aca954b`  
		Last Modified: Wed, 09 Nov 2022 17:37:09 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de19002dcea365821038023716e28374a8210ac45b5a63b539639130ad9b6bd8`  
		Last Modified: Wed, 09 Nov 2022 17:37:08 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc05d65ddfbc35592002f4ae7726cad3fa9b8777ac1f0cbb66bad8963c18cc7`  
		Last Modified: Wed, 09 Nov 2022 17:37:08 GMT  
		Size: 74.7 KB (74716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0517802e30312d5724623bf6cc9fe338f7330d522b267fad48ae4f85da52072`  
		Last Modified: Wed, 09 Nov 2022 17:37:06 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e343ab95fc3fdb7d230c1603a10283eddb85cd27b8150a2a2b45f7fe2e2b12`  
		Last Modified: Fri, 11 Nov 2022 01:18:55 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a32fc500579d83969db357545437c5b043f214ed396f14b88eaf9a2c037cc06`  
		Last Modified: Fri, 11 Nov 2022 01:19:16 GMT  
		Size: 193.2 MB (193165989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cce7c147f8b577fb92835f1a57fe030ba1a97cd1cdf7e4eb0ecfd9c6309a13`  
		Last Modified: Fri, 11 Nov 2022 01:18:56 GMT  
		Size: 3.8 MB (3781291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae03b6e161ec2b7923f68d122464a1ce681aa3d5fb90b3a9d210475b03a6869`  
		Last Modified: Fri, 11 Nov 2022 01:18:55 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
