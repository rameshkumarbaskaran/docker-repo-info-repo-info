## `eclipse-temurin:19-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:1bb03e892f4da14619aaae66a82cf46b230400f0e05f3b0dfdbd10b3bcda1943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `eclipse-temurin:19-nanoserver-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:8a029c79fa84b6b139fa5c0c3c0a73f09a4b05cfab9a45427afd98c1b775e448
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.4 MB (311444076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683ce923efb13e186352c7a8b13b23c4832936bcf1eca6982d26e24a7439ea1c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Sep 2022 20:11:22 GMT
RUN Apply image 10.0.20348.1006
# Wed, 14 Sep 2022 16:38:20 GMT
SHELL [cmd /s /c]
# Mon, 26 Sep 2022 23:28:21 GMT
ENV JAVA_VERSION=jdk-19+36
# Mon, 26 Sep 2022 23:28:22 GMT
ENV JAVA_HOME=C:\openjdk-19
# Mon, 26 Sep 2022 23:28:23 GMT
USER ContainerAdministrator
# Mon, 26 Sep 2022 23:28:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Mon, 26 Sep 2022 23:28:38 GMT
USER ContainerUser
# Mon, 26 Sep 2022 23:28:54 GMT
COPY dir:f9e4978cc3e169a38f06094f4d9bd0ec177b4256ff40cd3387fc1d393235d05c in C:\openjdk-19 
# Mon, 26 Sep 2022 23:29:16 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 26 Sep 2022 23:29:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:09629875cd6ee57fa551626fa2963d8b54718ba9acbf28e7cb5d684a9cb754d7`  
		Size: 118.1 MB (118131331 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:07f30e2ceaa03f6ac7b6e6f319083288f48d1fa2a61f36f51f516da241496976`  
		Last Modified: Wed, 14 Sep 2022 16:57:28 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864919bef3913744b28c53273341a0b0ec4a3c1785d5140ac9f4e3e94e1a5578`  
		Last Modified: Mon, 26 Sep 2022 23:35:22 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc56ee6307a1b64af8969055dbc830e5ff5920fa53ebd6eb48accb9ab328499`  
		Last Modified: Mon, 26 Sep 2022 23:35:22 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402c82e82d21c41f5c1a221c457c0fde325671f19b742915fd2772c5fb8ab083`  
		Last Modified: Mon, 26 Sep 2022 23:35:22 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef34e0a52f3fadf98a0ccef1daf4579718ab2d54cdd9cdf7613fe123578a90bb`  
		Last Modified: Mon, 26 Sep 2022 23:35:20 GMT  
		Size: 80.5 KB (80480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9149f802f4ccb5a15b71877a120f3968cfefd4bc9d29f9732a691572ccbc2c`  
		Last Modified: Mon, 26 Sep 2022 23:35:20 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8ffe94dd1ceabd0eb71d354637c43b6e02d4bce509efd8708fd1361ff0d6ba`  
		Last Modified: Mon, 26 Sep 2022 23:35:40 GMT  
		Size: 193.2 MB (193162297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdb73422e29c8fa192f29874017bb6f8b64f3f315f8f377313874208f8c8fbf`  
		Last Modified: Mon, 26 Sep 2022 23:35:20 GMT  
		Size: 63.1 KB (63122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48fa9c790564d1282c5246c19c0f24284a094ab082aa941fa1fb3b4cd3281ca`  
		Last Modified: Mon, 26 Sep 2022 23:35:20 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
