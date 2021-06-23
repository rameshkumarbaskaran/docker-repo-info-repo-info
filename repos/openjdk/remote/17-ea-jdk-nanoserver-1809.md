## `openjdk:17-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:12a67b820999f08c5af1db55da094bbdc4d9919bde0006209a4b1cc3245ca480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `openjdk:17-ea-jdk-nanoserver-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull openjdk@sha256:e30106f1a7ebb4cccc804af6ccb4f98d66ca31d8f5fce0cdbbba873241a736cb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288511479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a875656d52726a69e76aac51435a4fdb92f94ab8fd10840d1fed639e202651d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 16:52:42 GMT
SHELL [cmd /s /c]
# Wed, 09 Jun 2021 16:52:44 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Jun 2021 16:52:46 GMT
USER ContainerAdministrator
# Wed, 09 Jun 2021 16:53:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Jun 2021 16:53:09 GMT
USER ContainerUser
# Tue, 22 Jun 2021 21:27:23 GMT
ENV JAVA_VERSION=17-ea+27
# Tue, 22 Jun 2021 21:27:40 GMT
COPY dir:9ee87eefb484410cd699ce54437907739187361b19c03f46b6a41ed66436fb27 in C:\openjdk-17 
# Tue, 22 Jun 2021 21:28:00 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 22 Jun 2021 21:28:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e4800203e906d49fbdaf1eeab4de72f28796d5b9a1ea44f8d7461001cfa56614`  
		Size: 102.7 MB (102671454 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:acc28506464ab4d21eaffeb562876f3408463a46d298d12ded7ac0e3dd3c1bd6`  
		Last Modified: Wed, 09 Jun 2021 17:25:28 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a017ad6d2c865b2b606d1d084d50c43233147ea5cf53857802c790c6c01b7c3`  
		Last Modified: Wed, 09 Jun 2021 17:25:26 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c3e213028246803502d07da137fca93406b7b31a282ab02ef95a4e7547b1e1`  
		Last Modified: Wed, 09 Jun 2021 17:25:26 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24145c50d278aaa44ac5a4bc31c1b03bac6fcd0d7e2d291c01685bc9b4260369`  
		Last Modified: Wed, 09 Jun 2021 17:25:26 GMT  
		Size: 69.6 KB (69634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0442665d8729ebbf2ff71dbd067a8b13f6af08edd7d070d9ba24a2e9e30285f8`  
		Last Modified: Wed, 09 Jun 2021 17:25:24 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e332134b2594e21c2607bcccb3b001a8d4e9764590f5bee239245fd0788ace20`  
		Last Modified: Tue, 22 Jun 2021 21:39:33 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67f92b34e6ac4fdc5812bd013be6ae5bdbdb6d86d2686ba558b5312b50c0d02`  
		Last Modified: Tue, 22 Jun 2021 21:42:52 GMT  
		Size: 182.1 MB (182119237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc51d8af87e0514784f8a70d9f8bb7a7604de094811f96a749ba4f9fe73ac0a4`  
		Last Modified: Tue, 22 Jun 2021 21:39:37 GMT  
		Size: 3.6 MB (3644199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8130f4e8ab8cd2a8fce4094c251ebe2c8192be3606aadef7d395b01884ee3fe1`  
		Last Modified: Tue, 22 Jun 2021 21:39:33 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
