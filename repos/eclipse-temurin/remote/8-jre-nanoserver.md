## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:7bc2bc14c9caf5cfb4e97106f48a05f9a4082ab3daf536aee34d869d5712d78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.524; amd64
	-	windows version 10.0.17763.2565; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.524; amd64

```console
$ docker pull eclipse-temurin@sha256:854ed51bb1bd9552900a09df95c27de31ecd4e7127989efd5b5a02551f6660e6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156722049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd35202967cbecc3114b48664bb31bdae6eba23556ed1f51e254bb5e41825b56`
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
# Wed, 09 Feb 2022 20:21:08 GMT
COPY dir:d1a6722e8aa7d48dd5f1c45f802460fd028688b69665fdd4cb7519baa4fcb589 in C:\openjdk-8 
# Wed, 09 Feb 2022 20:21:22 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:cfb331464ee23445eb36b27d9cca511b74b2ea78deb712b6511decdcaee9a994`  
		Last Modified: Thu, 10 Feb 2022 21:15:39 GMT  
		Size: 39.1 MB (39110130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac8d663d75f4a3d8a7cef821a57c9676ac1135babe3700dfe70a276de9724e3`  
		Last Modified: Thu, 10 Feb 2022 21:15:33 GMT  
		Size: 61.6 KB (61616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.17763.2565; amd64

```console
$ docker pull eclipse-temurin@sha256:10d58a9b61c585c70e6418ce599c450a478b5f7549bf64b8b784578f14400d5b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142335965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6822f766c2d0dcb3f0590ac5d175744be85ea6ba304a3dc6e737d73c36788f0`
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
# Wed, 09 Feb 2022 19:53:03 GMT
COPY dir:d1a6722e8aa7d48dd5f1c45f802460fd028688b69665fdd4cb7519baa4fcb589 in C:\openjdk-8 
# Wed, 09 Feb 2022 19:53:15 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:5c7c71e51e98e4c136cde1ebfc42d70bfb82de30a910c0285071a6e1fb93be71`  
		Last Modified: Thu, 10 Feb 2022 20:39:03 GMT  
		Size: 39.1 MB (39109246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f322e1f3abd04ed04de70f26b16006662eb0d6ffa97672084d468d9949d8326`  
		Last Modified: Thu, 10 Feb 2022 20:38:57 GMT  
		Size: 55.7 KB (55723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
