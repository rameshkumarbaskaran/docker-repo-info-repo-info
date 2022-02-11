## `eclipse-temurin:8u322-b06-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ef9f295f1aee9a0ae1b5dcb019bcd5759730532504303cf32356fff984f1b47d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.524; amd64
	-	windows version 10.0.17763.2565; amd64

### `eclipse-temurin:8u322-b06-jdk-nanoserver` - windows version 10.0.20348.524; amd64

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

### `eclipse-temurin:8u322-b06-jdk-nanoserver` - windows version 10.0.17763.2565; amd64

```console
$ docker pull eclipse-temurin@sha256:2fad30814cf22b189faca86889294acf1fa987b35d81a868e05db73275345a1d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203438826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d588e218a9c519254297215d0b307ca2bf21888df6ded34450ec37265f68e488`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:45:32 GMT
SHELL [cmd /s /c]
# Wed, 09 Feb 2022 19:48:23 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 09 Feb 2022 19:48:24 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Feb 2022 19:48:25 GMT
USER ContainerAdministrator
# Wed, 09 Feb 2022 19:48:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Feb 2022 19:48:35 GMT
USER ContainerUser
# Wed, 09 Feb 2022 19:48:50 GMT
COPY dir:7138e59caf0c25d74e2c65f3638e655f7739a280619af2a4072fd7cd5d6cb20c in C:\openjdk-8 
# Wed, 09 Feb 2022 19:49:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5a7f567e84a5a148036156650a47ef7eec0187f17e880d3b475e51dacd70077b`  
		Last Modified: Wed, 09 Feb 2022 19:20:50 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50eec118482da18ebcf041e946d2ecdd4d786d3199822a1b1e4cf886efc8a15f`  
		Last Modified: Thu, 10 Feb 2022 20:36:52 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf7548ea2604040a9d073982ec0a79e3bf50442a922582d5b24d447eebaa08d`  
		Last Modified: Thu, 10 Feb 2022 20:36:52 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7423920bceb35cc62ab0ffc3a4be41829b7e0976b7c25d2f1adef45843ee49e8`  
		Last Modified: Thu, 10 Feb 2022 20:36:49 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586c60c649979b6d6f260501b5a19fe018f13a9e4a59586a3ccec88cc7bbd43e`  
		Last Modified: Thu, 10 Feb 2022 20:36:49 GMT  
		Size: 78.1 KB (78106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f1e2c6f79e2d947ef8e40e6b08de9fd3bac072f460f4eaa6d5125169b2197f`  
		Last Modified: Thu, 10 Feb 2022 20:36:49 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8668a1b6d9bea12bd94adb97cc62c5d5d6b6d8cb658d180e450f8fbe9391fe`  
		Last Modified: Thu, 10 Feb 2022 20:37:02 GMT  
		Size: 100.2 MB (100202951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4e53f0d1c3633d3736af519cfcd9a45e08c4972e4e4ee45b70e2f5101171b7`  
		Last Modified: Thu, 10 Feb 2022 20:36:49 GMT  
		Size: 64.9 KB (64879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
