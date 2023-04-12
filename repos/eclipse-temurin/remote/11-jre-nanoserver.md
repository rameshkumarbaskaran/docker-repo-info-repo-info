## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:4ce18825cb7622d5515fd871f0402f803859cda20bea25ff2dffa508c3482316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1668; amd64
	-	windows version 10.0.17763.4252; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.1668; amd64

```console
$ docker pull eclipse-temurin@sha256:6f6d7ea7cc627e9ee30f306bc5557a11888c8fcff0125c06f5971609ab247e34
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165605216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5f7135469b50ac56e6089267542055d2817259a34de6aad0e747c65126adfa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 12 Apr 2023 01:45:24 GMT
COPY dir:ae8209dfc1a9f024f854c3514bc0c0906475eaa2bd640116685865d2510e5d91 in C:\openjdk-11 
# Wed, 12 Apr 2023 01:45:39 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:6ac41eee80eb6b7636477682dab0e57c7e5fc931c7ee357a5e0557cb919257b1`  
		Last Modified: Wed, 12 Apr 2023 09:46:58 GMT  
		Size: 43.1 MB (43137164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a72d8ad17aaf8c7f6d9cdcf150375ed52001f5d533688a81636d2d9c10b058c`  
		Last Modified: Wed, 12 Apr 2023 09:46:49 GMT  
		Size: 61.8 KB (61754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.4252; amd64

```console
$ docker pull eclipse-temurin@sha256:ad86bfb10a5deadd5a0c4b6991b812807c1e5cf014d23910aa3ffb84b7f37c45
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150080424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6613ebe0e07e006f87d5dd4ab7d3c4408c514f2fe213c7e7021d693af30d79ec`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 12 Apr 2023 01:18:48 GMT
COPY dir:ae8209dfc1a9f024f854c3514bc0c0906475eaa2bd640116685865d2510e5d91 in C:\openjdk-11 
# Wed, 12 Apr 2023 01:19:06 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:f8eccbb4515c4219db58d7e5ab4bdd56a6b53caa980faaedadb5e911bd03ba77`  
		Last Modified: Wed, 12 Apr 2023 09:39:22 GMT  
		Size: 43.1 MB (43137319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10756eed56406e24b5ad80676be5d372409722b38bb35149aeb2f63187c16fd`  
		Last Modified: Wed, 12 Apr 2023 09:39:13 GMT  
		Size: 80.3 KB (80281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
