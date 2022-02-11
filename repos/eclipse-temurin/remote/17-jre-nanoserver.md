## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:37ae74467edb2521515b6835661a9b22a8896328fd6d50e17b13171278f99d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.524; amd64
	-	windows version 10.0.17763.2565; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.524; amd64

```console
$ docker pull eclipse-temurin@sha256:8bc3ba0e8d8e11915ee20403def99ecd1536ed34e40e93e43142ff45a79b9e08
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160715587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5afa2f07e3ce52a70de0e4631cc13bd0105184b8f83f2dd0eb16971854c1d2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 01 Feb 2022 02:25:40 GMT
RUN Apply image ltsc2022-amd64
# Wed, 09 Feb 2022 20:19:59 GMT
SHELL [cmd /s /c]
# Wed, 09 Feb 2022 20:23:11 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Wed, 09 Feb 2022 20:23:12 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Feb 2022 20:23:13 GMT
USER ContainerAdministrator
# Wed, 09 Feb 2022 20:23:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Feb 2022 20:23:23 GMT
USER ContainerUser
# Wed, 09 Feb 2022 20:24:34 GMT
COPY dir:7a64f3064f2760e9a3a0ea5871812392dd639be8dd87901cbb720c404830d2a7 in C:\openjdk-17 
# Wed, 09 Feb 2022 20:24:46 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3ab33c1d9cc1eaef56d5617b87373ead45d8a4ff7ab7da384afe612ba569a524`  
		Size: 117.5 MB (117457656 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3caa1e550ae326513f81130f539f06a05b30aca3f6ac96039cce37a715c5f008`  
		Last Modified: Thu, 10 Feb 2022 21:15:09 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c137f6d443ab391dba81e3ea945e6ef6f4b3abe558872170a36ce7d1491c369`  
		Last Modified: Thu, 10 Feb 2022 21:19:57 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2cc915fa9de18f231edb0d38aaec021a7704c97fea59e3924ae50ec434b423`  
		Last Modified: Thu, 10 Feb 2022 21:19:57 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd1f04355408f8d28280a3e5e77355eb637128027fe3fe102eb9f1508aad7be1`  
		Last Modified: Thu, 10 Feb 2022 21:19:57 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e75318cd44ff95d4b5b1f45c1db4a0f9424efbbcda05b14b92ed4a295d0f86`  
		Last Modified: Thu, 10 Feb 2022 21:19:55 GMT  
		Size: 84.0 KB (83998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bacd5585314d12d6a114a0baae148677958f857e374bb2a23fffd6a575ff726`  
		Last Modified: Thu, 10 Feb 2022 21:19:55 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa212b4c5f6622b08a09a11d45e82e17bd7962dad56af9535eefc8857091e79`  
		Last Modified: Thu, 10 Feb 2022 21:24:04 GMT  
		Size: 43.1 MB (43106380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa322d2504aa455505a0899701db691c075085b33f6d742f9eb2981312f40d49`  
		Last Modified: Thu, 10 Feb 2022 21:23:20 GMT  
		Size: 61.8 KB (61769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.2565; amd64

```console
$ docker pull eclipse-temurin@sha256:0c1774818432a434e95af596c6ca91a266aa9db77d93da04ee04b8735d7459cd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149307310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c6e939d1662adbf6c39d53cf724e188de9b5a43a1cb5d67ac92fc7b7b84be4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:45:32 GMT
SHELL [cmd /s /c]
# Wed, 09 Feb 2022 20:14:27 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Wed, 09 Feb 2022 20:14:28 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Feb 2022 20:14:28 GMT
USER ContainerAdministrator
# Wed, 09 Feb 2022 20:14:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Feb 2022 20:14:38 GMT
USER ContainerUser
# Wed, 09 Feb 2022 20:19:31 GMT
COPY dir:7a64f3064f2760e9a3a0ea5871812392dd639be8dd87901cbb720c404830d2a7 in C:\openjdk-17 
# Wed, 09 Feb 2022 20:19:53 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5a7f567e84a5a148036156650a47ef7eec0187f17e880d3b475e51dacd70077b`  
		Last Modified: Wed, 09 Feb 2022 19:20:50 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff9a6949b337ee2cf8190807249bcc9fa8f67cfd1d72a4371750bf483cde6ce`  
		Last Modified: Thu, 10 Feb 2022 21:12:53 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a85abfd5586f64024d88a765fd0921366b7b31d57f0dccf45f0607844c1f8e5`  
		Last Modified: Thu, 10 Feb 2022 21:12:53 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ddbe55c6acad01f3f736dd4e0a2f376883cb43b47086f1440abb55839fb1c6`  
		Last Modified: Thu, 10 Feb 2022 21:12:53 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a0583e34d0ca468f6787b83d5f06f152331457e865656536ca50644678e191`  
		Last Modified: Thu, 10 Feb 2022 21:12:50 GMT  
		Size: 70.2 KB (70234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5dbb6c04a70d0d5eb61cda171231a7dd89010832f12bfe06ad89e81be06eae4`  
		Last Modified: Thu, 10 Feb 2022 21:12:50 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63522a2a51f9c14f96461789d87de2445b9105a2974612d9ba66bc4c1c3f8d`  
		Last Modified: Thu, 10 Feb 2022 21:14:57 GMT  
		Size: 43.1 MB (43103535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cffc5b00cf0934e0869e143587b9233fb215e706ff6cb7f9d8e8c2dbbec023`  
		Last Modified: Thu, 10 Feb 2022 21:14:16 GMT  
		Size: 3.0 MB (3040653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
