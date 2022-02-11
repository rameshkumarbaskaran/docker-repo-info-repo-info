## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:e7194c86352007ad7186208d1fe230a03005dc93d86fa62ca31f304f13e3fe89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.524; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.524; amd64

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
