## `eclipse-temurin:8-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:736d49042a2efc180d06f82dee2de752e9afb08a706aca4dc56d36b00782c103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.524; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.524; amd64

```console
$ docker pull eclipse-temurin@sha256:772b74dd5f23d4b45abce988deaab021612edf03fc691bb68f176a909ae8e2bc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217825377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310ecf9b9c145e2596c198fe43fe27da0fb12a1c90416be74aeaa9738140ff06`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 01 Feb 2022 02:25:40 GMT
RUN Apply image ltsc2022-amd64
# Wed, 09 Feb 2022 20:19:59 GMT
SHELL [cmd /s /c]
# Wed, 09 Feb 2022 20:20:00 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 09 Feb 2022 20:20:01 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Feb 2022 20:20:02 GMT
USER ContainerAdministrator
# Wed, 09 Feb 2022 20:20:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Feb 2022 20:20:19 GMT
USER ContainerUser
# Wed, 09 Feb 2022 20:20:36 GMT
COPY dir:7138e59caf0c25d74e2c65f3638e655f7739a280619af2a4072fd7cd5d6cb20c in C:\openjdk-8 
# Wed, 09 Feb 2022 20:20:52 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3ab33c1d9cc1eaef56d5617b87373ead45d8a4ff7ab7da384afe612ba569a524`  
		Size: 117.5 MB (117457656 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3caa1e550ae326513f81130f539f06a05b30aca3f6ac96039cce37a715c5f008`  
		Last Modified: Thu, 10 Feb 2022 21:15:09 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9d47041d8eb8952fea9ea72a4df2e7dd3394491d4def0a3e6a199df12137a0`  
		Last Modified: Thu, 10 Feb 2022 21:15:09 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e53ad2dce517acf107b59cae527aba58f36f3dcf4d32b681fff54926f30906`  
		Last Modified: Thu, 10 Feb 2022 21:15:09 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72d0dbb298b0dea8bcc27f38fb8b42ae0d8924d9dabb751ac680ffe99eab93a`  
		Last Modified: Thu, 10 Feb 2022 21:15:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26583295562e92cfb91e831286e820012800d788187a744880ba0dec8924515a`  
		Last Modified: Thu, 10 Feb 2022 21:15:07 GMT  
		Size: 86.8 KB (86827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a88f56e15510503f95689879feb6d9556379a006598b3c891a8480a64c612a`  
		Last Modified: Thu, 10 Feb 2022 21:15:07 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a939d94ef12454eec834837931bad7c4e33038596ef107e16d0f8abcef3a5f40`  
		Last Modified: Thu, 10 Feb 2022 21:15:18 GMT  
		Size: 100.2 MB (100212665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7fe00a07fd9f33cab11f13dc981f40d947b29ae5976cc85d24603453f18cb8`  
		Last Modified: Thu, 10 Feb 2022 21:15:06 GMT  
		Size: 62.4 KB (62409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
