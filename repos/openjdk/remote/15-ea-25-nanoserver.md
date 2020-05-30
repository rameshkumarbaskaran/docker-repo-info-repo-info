## `openjdk:15-ea-25-nanoserver`

```console
$ docker pull openjdk@sha256:5ebc3f5abe8265888ff224daddd527ddc0160a06236173ba0aa631ac7ec4920f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `openjdk:15-ea-25-nanoserver` - windows version 10.0.17763.1217; amd64

```console
$ docker pull openjdk@sha256:68646cdd2a64e38e6b2bffcb265a9eac71355e2cd82e4fcafa1354afdfb99d89
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295535885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02828f6cf83f22262f97ab357362f827e3aa5ee890d8d49d752d1b8b31e9a15b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 06 May 2020 12:39:06 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 15:30:41 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2020 15:30:42 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 13 May 2020 15:30:43 GMT
USER ContainerAdministrator
# Wed, 13 May 2020 15:31:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 13 May 2020 15:31:01 GMT
USER ContainerUser
# Sat, 30 May 2020 00:18:43 GMT
ENV JAVA_VERSION=15-ea+25
# Sat, 30 May 2020 00:19:31 GMT
COPY dir:3a8aeded82e7f61ca88e0ff8145e69c401c128500e4ce2b1c50e665656370f37 in C:\openjdk-15 
# Sat, 30 May 2020 00:19:54 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Sat, 30 May 2020 00:19:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b9e6fec25718aef5ed18d499b27e43adb524f9ee4f2eb3f0fffaea018e7e86b0`  
		Size: 101.0 MB (101019852 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3c597e8fceaeb76628095f6dcfa538d497e85739068a817b45d73be2b96a3b37`  
		Last Modified: Wed, 13 May 2020 16:09:16 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe4a1ac076e1dee08c07748ed0bf748357ec3c058f29131ddb0c6903b01c5b3`  
		Last Modified: Wed, 13 May 2020 16:09:16 GMT  
		Size: 837.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00cb774af18b914ba24ccfaba030aaee1af53cc965b45edd9166b2cbdc59558`  
		Last Modified: Wed, 13 May 2020 16:09:15 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0bbbe06e51300ecf6f12747f98fa77f8b3370196f85b87015dca501577f4aa`  
		Last Modified: Wed, 13 May 2020 16:09:14 GMT  
		Size: 64.1 KB (64131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0840576e1fb16bf2edf823eb58f597b05345e558ebba64301d718163d95b93d`  
		Last Modified: Wed, 13 May 2020 16:09:12 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2b4ab64030f0a7470cc8ac4342e6376d21e2e9ab4a6bdfc686bcf192d855d3`  
		Last Modified: Sat, 30 May 2020 00:25:41 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245f19ff41a9a4b83f9c86b1671dcaf14da3b29e2f0f550471a81d8624879020`  
		Last Modified: Sat, 30 May 2020 00:26:43 GMT  
		Size: 190.9 MB (190940836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0386788c81b870a47d9a31720fb54fe9adfef7df4878b04a2d8525edef8c56c9`  
		Last Modified: Sat, 30 May 2020 00:25:42 GMT  
		Size: 3.5 MB (3505713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f896a7b3e24fd78a153a33540445d93664fed16748530bfa9ccaa1343a3e7dcc`  
		Last Modified: Sat, 30 May 2020 00:25:41 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
