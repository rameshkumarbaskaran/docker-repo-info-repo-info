## `eclipse-temurin:17-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:24b4ac5a73688a57e7c0236fc67f2bdbf2b2f37ae0a0ad4b14a999ab5171e141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `eclipse-temurin:17-jdk-nanoserver-1809` - windows version 10.0.17763.4252; amd64

```console
$ docker pull eclipse-temurin@sha256:aca26b491d93e68003953bd976d6ea10369ef94ebfe40b85905ec73fe8923aa5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (296008695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442c200f322b7883cf286e9dd91c9f85a525d358ea267796d9dd38de02fe8ef8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Tue, 11 Apr 2023 23:45:41 GMT
SHELL [cmd /s /c]
# Wed, 12 Apr 2023 01:25:11 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Wed, 12 Apr 2023 01:25:12 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Apr 2023 01:25:13 GMT
USER ContainerAdministrator
# Wed, 12 Apr 2023 01:25:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Apr 2023 01:25:24 GMT
USER ContainerUser
# Wed, 12 Apr 2023 01:25:39 GMT
COPY dir:b9d1887161cde3cc24ae2101d8a284bfc20814b15fed427bc1c905c1248fb0bf in C:\openjdk-17 
# Wed, 12 Apr 2023 01:25:59 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Apr 2023 01:26:00 GMT
CMD ["jshell"]
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
	-	`sha256:9d940edd2c169dbe97e28eaac688f773a26971f49cbce0c580dec219c0a091a6`  
		Last Modified: Wed, 12 Apr 2023 09:40:59 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68cf891bc434751fa3e0d43803d1d1b3966b15191058fd5bf2d9f3f70340008`  
		Last Modified: Wed, 12 Apr 2023 09:40:59 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1662ed07c1d02bbfbbd979a470af707c2e65c7d8de779c6e791ca43a34f7ec`  
		Last Modified: Wed, 12 Apr 2023 09:40:59 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2804a413fa32f1ac8096607d75ad6a983b2755f9d7994a3275faa45ad68b44`  
		Last Modified: Wed, 12 Apr 2023 09:40:57 GMT  
		Size: 71.3 KB (71299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddad53a51d13c426f8e7d899d76b648e9ca0201514f6c69c5335ffc180da6eb0`  
		Last Modified: Wed, 12 Apr 2023 09:40:56 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b25cf6e88454497cad74f97cd7b257e75b668c766d93adb969ea922db64f874`  
		Last Modified: Wed, 12 Apr 2023 09:41:18 GMT  
		Size: 185.5 MB (185476505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7939fd9463285685a5ae3cbbc0542c20afb3684f0541f7e28f9c67033f06d1e`  
		Last Modified: Wed, 12 Apr 2023 09:40:58 GMT  
		Size: 3.7 MB (3665042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e92f69836767d591945350f6170936fa85287b8dfc2f3143605d9f2a0e3c4fc`  
		Last Modified: Wed, 12 Apr 2023 09:40:56 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
