## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:a387634abf2a7e8aacd7e5a5e1ff0c4412deb74d0dd721d76e8f320b2768c15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.524; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.524; amd64

```console
$ docker pull eclipse-temurin@sha256:8e455f16d573d4167fe617e47354735c9673d3023b8bffdd3faea8920ac718f7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160385863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8373ef20d64913efe3ddce057f533ee4a7c99c94432a08902d31a6e3d91ed95`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 01 Feb 2022 02:25:40 GMT
RUN Apply image ltsc2022-amd64
# Wed, 09 Feb 2022 20:19:59 GMT
SHELL [cmd /s /c]
# Thu, 10 Feb 2022 20:28:59 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Thu, 10 Feb 2022 20:29:00 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 10 Feb 2022 20:29:00 GMT
USER ContainerAdministrator
# Thu, 10 Feb 2022 20:29:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Feb 2022 20:29:14 GMT
USER ContainerUser
# Thu, 10 Feb 2022 20:30:22 GMT
COPY dir:7b430082d92796c7933d8991df8414f6ea317b19767304be325fe29c5d7cc52a in C:\openjdk-11 
# Thu, 10 Feb 2022 20:30:34 GMT
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
	-	`sha256:ee90641fd683fd62c7683c0eeed2f467a3eba23e2fe31fd595f8a1c980d89545`  
		Last Modified: Thu, 10 Feb 2022 21:15:51 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b362a9e00c369a12ed7e8d91ce6fa54248e8bc11ac9834f1debb1c7061e7b0b1`  
		Last Modified: Thu, 10 Feb 2022 21:15:51 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777a63efdac0dbd77fb28e3a91bf1e111cc91082639433992439cf1a2d061e1a`  
		Last Modified: Thu, 10 Feb 2022 21:15:51 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765baba86fc9ffb96ce8448a6ca1330c02e348a00ebf99927d953d2f726fa658`  
		Last Modified: Thu, 10 Feb 2022 21:15:49 GMT  
		Size: 89.3 KB (89255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44abd88b172f82a165ec0247add2c9ac0c56979ed9eefc19a6df6b3bc5434abc`  
		Last Modified: Thu, 10 Feb 2022 21:15:49 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480e19059a3ffc3927602db378a8bc81f299fafedd91e8e9f7919eb594adc3c9`  
		Last Modified: Thu, 10 Feb 2022 21:19:45 GMT  
		Size: 42.8 MB (42759983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a60069ba3f9dbaf2312e3b9cdfd3bfaedb63fe62b7ac80837f50f76261b571`  
		Last Modified: Thu, 10 Feb 2022 21:19:37 GMT  
		Size: 73.2 KB (73167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
