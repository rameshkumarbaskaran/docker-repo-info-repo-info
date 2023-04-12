## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:e08c34040dd6fe1a7be178a121ed09df1e880a076dc11e888ba9d25a1193085b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1668; amd64
	-	windows version 10.0.17763.4252; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.1668; amd64

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

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.17763.4252; amd64

```console
$ docker pull eclipse-temurin@sha256:f91c459c6fcf21f9be1cd5aa178535c29a32bb7daa4f0a62ddad80ef68adb263
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.9 MB (299858474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3982158a0739f0fb2ef55733265aec5e055df0a7fc5233dbb36bc1da67f5f4b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Tue, 11 Apr 2023 23:45:41 GMT
SHELL [cmd /s /c]
# Wed, 12 Apr 2023 01:12:51 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Wed, 12 Apr 2023 01:12:52 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 12 Apr 2023 01:12:52 GMT
USER ContainerAdministrator
# Wed, 12 Apr 2023 01:13:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Apr 2023 01:13:05 GMT
USER ContainerUser
# Wed, 12 Apr 2023 01:13:20 GMT
COPY dir:3631bd3b4ae70db635b51d6f7ad3f3254aa758db5b0d079379d506c898ecba14 in C:\openjdk-11 
# Wed, 12 Apr 2023 01:13:42 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Apr 2023 01:13:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af799fb2ff133c89311c6a42d34b8cb6c9b11d775f52e04ab08389d05e64ed1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:10 GMT  
		Size: 106.8 MB (106788951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1db438f20b81fe0c031e4e3eee58d278fba7258d01057ff18964cccf70d41c`  
		Last Modified: Wed, 12 Apr 2023 00:52:38 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c14d46dd41fe0a71b26954ba858ba5a0be2788dcd2f3dc4442005c674202560`  
		Last Modified: Wed, 12 Apr 2023 09:38:01 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c327c01dd0740e929779e9e68a59007959b0b1149e3b1b1699df69103ef0f853`  
		Last Modified: Wed, 12 Apr 2023 09:38:01 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27217dd5debb83c3793d0d13ee9e14daa08ac3e972dba97ed5398759f8f8c50b`  
		Last Modified: Wed, 12 Apr 2023 09:38:01 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d516c98f6c6768c5a7b9a28d5aaaefbd5424dff108cc0476b4cd43e793257a8a`  
		Last Modified: Wed, 12 Apr 2023 09:37:59 GMT  
		Size: 68.2 KB (68167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550c019360100df3733869fb191bb12c59de1b6dcc22f7df80b645ff26bbb8aa`  
		Last Modified: Wed, 12 Apr 2023 09:37:59 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:967c840c428e6632c97560dcbb24ac63a3a0ad4308605b291c78056b6a84966e`  
		Last Modified: Wed, 12 Apr 2023 09:38:20 GMT  
		Size: 192.9 MB (192904450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af59beef586af14b596a28e62cc5f55b8d62ffa9c48eaabcd1b90fdcad871bb`  
		Last Modified: Wed, 12 Apr 2023 09:37:59 GMT  
		Size: 90.0 KB (90042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f61e4a974e5f03077a930bd0869bb5b60023ea8d31bcbd7de70069223a5b0b3`  
		Last Modified: Wed, 12 Apr 2023 09:37:59 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
