## `eclipse-temurin:8u362-b09-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:e364b89d664d96ccc994d4c69e0414d76e519b3a46c90e518fa233c00fa2b759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `eclipse-temurin:8u362-b09-jre-nanoserver-1809` - windows version 10.0.17763.4252; amd64

```console
$ docker pull eclipse-temurin@sha256:453f5b6f12b9d36d7be1825babfd50f15ef7fb8181cb5508c1eb84db680e4956
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146877208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1921031b1c6d28aa1a1aca43870455913e3fc812c0b896eefc7267e2fd3b6795`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Tue, 11 Apr 2023 23:45:41 GMT
SHELL [cmd /s /c]
# Wed, 12 Apr 2023 01:00:37 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 12 Apr 2023 01:00:38 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Apr 2023 01:00:39 GMT
USER ContainerAdministrator
# Wed, 12 Apr 2023 01:00:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Apr 2023 01:00:54 GMT
USER ContainerUser
# Wed, 12 Apr 2023 01:06:43 GMT
COPY dir:dcd2674e91fb412db18990a7004f7a484148b702bd6de08f5ae3a3d6f6a3f6f8 in C:\openjdk-8 
# Wed, 12 Apr 2023 01:06:56 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:d5593d7ff65e071c973825c7d57969b7431518490174383b2cc83b5272296d69`  
		Last Modified: Wed, 12 Apr 2023 09:35:19 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da43b0e68ac3ed536edc3110c6c369d90f6c8ce83d22fd01c21b77883982994`  
		Last Modified: Wed, 12 Apr 2023 09:35:19 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5798c8a6554f2ad678b5090d67918fc66af0fa922dc37577a0c3c135241264d4`  
		Last Modified: Wed, 12 Apr 2023 09:35:17 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda7d4d02f9e02ded3b5495fee94a3bf6dfaad7271d7fb26f996d061ac4747c4`  
		Last Modified: Wed, 12 Apr 2023 09:35:17 GMT  
		Size: 77.7 KB (77691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dacb99131be332bd145d4ed8040f668d972a74e3bc970e43283fdf3d6f61deb`  
		Last Modified: Wed, 12 Apr 2023 09:35:17 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52d150f1846e64bfab44761bc3691dbb29539ec0b91e252ef6e981878dc18d7`  
		Last Modified: Wed, 12 Apr 2023 09:36:25 GMT  
		Size: 39.9 MB (39947982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d41f0f1c7e1e3ce9156104db358c3d3c5470b0d9c3ec9723090ad1baa9555ee`  
		Last Modified: Wed, 12 Apr 2023 09:36:18 GMT  
		Size: 56.8 KB (56784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
