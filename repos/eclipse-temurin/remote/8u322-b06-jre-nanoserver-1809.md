## `eclipse-temurin:8u322-b06-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:15121fb516f20bf201039111069e79b2d794c7f99af007a7ae11d2276b18bded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `eclipse-temurin:8u322-b06-jre-nanoserver-1809` - windows version 10.0.17763.2565; amd64

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
