## `openjdk:14-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:8712166da6098609524f8b68a6ebe7e41f5a3568711a0a9992b6a1146e46e36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `openjdk:14-jdk-nanoserver` - windows version 10.0.17763.973; amd64

```console
$ docker pull openjdk@sha256:6524b580693b830cda86de74bcb383c29a7d5d28d4230973f81317c01e1267c5
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298439008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ccae489b27cfe2b9d945c7d50b577d543bbb6ad9b11273cf3f19f73c7a88c0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Tue, 14 Jan 2020 23:56:11 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2020 00:05:42 GMT
ENV JAVA_HOME=C:\openjdk-14
# Wed, 15 Jan 2020 00:05:43 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2020 00:05:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 15 Jan 2020 00:05:57 GMT
USER ContainerUser
# Sat, 18 Jan 2020 00:29:05 GMT
ENV JAVA_VERSION=14-ea+32
# Sat, 18 Jan 2020 00:30:03 GMT
COPY dir:6d398428d1bf0d08f66d93328faa4aa5faffb119dfddddf6eb3bcd748e4b6db6 in C:\openjdk-14 
# Sat, 18 Jan 2020 00:30:21 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Sat, 18 Jan 2020 00:30:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:764e25aa4e95684bd69a4d130dc1c729bfaef95293d9c76c4d2a12ced9e3a9ac`  
		Last Modified: Wed, 15 Jan 2020 01:51:06 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f3a5df9926db070e4016e42e49a7d9ce0131f528e644ae4388774831b6b46e`  
		Last Modified: Wed, 15 Jan 2020 01:58:21 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c21d67a14cad5558f706984eed7f97aaa2665e4b4cf1a7a1d21888c5e2c02a2`  
		Last Modified: Wed, 15 Jan 2020 01:58:20 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ffd38236cfc5913ab84e035b74a0bddf197bbfffdd8e9e8b151cc30bbf8adb`  
		Last Modified: Wed, 15 Jan 2020 01:58:20 GMT  
		Size: 66.5 KB (66486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8510d836b27dbac14cee7131c4209ebf2081c2ba957f75e05cbeff605e5320`  
		Last Modified: Wed, 15 Jan 2020 01:58:18 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84375af539cf02558c36e4354768b04d081d6c007b8ac07fd13300082d4b64ad`  
		Last Modified: Sat, 18 Jan 2020 00:45:01 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7fa781f27341467086ceb9c58aa706121d4d733fa8c76341f399d2cadb555a`  
		Last Modified: Sat, 18 Jan 2020 00:45:26 GMT  
		Size: 193.9 MB (193865956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3138fdbf61059b989c0bbc14aa956497e49f38d3b4c118727acbc5f52a3c79c4`  
		Last Modified: Sat, 18 Jan 2020 00:45:02 GMT  
		Size: 3.4 MB (3446610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a11119c4ce10730858551189c2f0cf0aea4d8109d103a8425cb4a4dd126c88`  
		Last Modified: Sat, 18 Jan 2020 00:45:01 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
