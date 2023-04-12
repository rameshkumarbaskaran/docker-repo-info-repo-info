## `eclipse-temurin:11-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:cb98ba13fc7383b10277b01907ee52828171c87e9daf5dec3b5264c8d8807f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1668; amd64

### `eclipse-temurin:11-nanoserver-ltsc2022` - windows version 10.0.20348.1668; amd64

```console
$ docker pull eclipse-temurin@sha256:3a946cb828efa0870849a2cf496db208a9d1cf1ce814049ef15cff29b7dee48d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.4 MB (315357009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11acc1aff844ab123bf7bb0eb8be53f68bdd40e621d63bbc448a1007d74ad9b6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:16 GMT
RUN Apply image 10.0.20348.1668
# Wed, 12 Apr 2023 01:42:21 GMT
SHELL [cmd /s /c]
# Wed, 12 Apr 2023 01:44:00 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Wed, 12 Apr 2023 01:44:01 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 12 Apr 2023 01:44:02 GMT
USER ContainerAdministrator
# Wed, 12 Apr 2023 01:44:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Apr 2023 01:44:15 GMT
USER ContainerUser
# Wed, 12 Apr 2023 01:44:31 GMT
COPY dir:3631bd3b4ae70db635b51d6f7ad3f3254aa758db5b0d079379d506c898ecba14 in C:\openjdk-11 
# Wed, 12 Apr 2023 01:45:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Apr 2023 01:45:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e06b772d586b58466a653b72002aee7c59496110e9ae402ff58f026e44452506`  
		Last Modified: Wed, 12 Apr 2023 02:34:14 GMT  
		Size: 122.3 MB (122328782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8058ec80ac2516d001291dea383d4abfa22416397a4c869e6fd79c0d4b64565f`  
		Last Modified: Wed, 12 Apr 2023 09:45:40 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340a57ba2a31c55678f9ab219e70043913a0a38cb864da83746007f5aacb0224`  
		Last Modified: Wed, 12 Apr 2023 09:46:19 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd482821e4bde1aa059e720ef58bf7725923f37bb088d43a141ed48736106bf`  
		Last Modified: Wed, 12 Apr 2023 09:46:19 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7949db6d90f257b399b4553061a2cbc91da3b7c6d14a33d7b8d41d9737c3c217`  
		Last Modified: Wed, 12 Apr 2023 09:46:19 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ba0d6728a98a7755f89e51cf9a6412f2cfe66873b3b156664d8aad33c49413`  
		Last Modified: Wed, 12 Apr 2023 09:46:17 GMT  
		Size: 72.2 KB (72211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12619833c61d33858d3acfb41f405b5f1390f456ce0cd7e931922076109bf9b`  
		Last Modified: Wed, 12 Apr 2023 09:46:17 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc1e6d745a78b20b50e3f46762668a0543dcc586730078bfc5040be315cce68`  
		Last Modified: Wed, 12 Apr 2023 09:46:38 GMT  
		Size: 192.9 MB (192886922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc776f57da971b73a5800691a91138e006142a85cdf943ca606b13c2c14eded7`  
		Last Modified: Wed, 12 Apr 2023 09:46:17 GMT  
		Size: 62.7 KB (62730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebfc435c5f4f29adc7fa883f3def22985594c34358b82d19fd6ffa4641d8ee6`  
		Last Modified: Wed, 12 Apr 2023 09:46:17 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
