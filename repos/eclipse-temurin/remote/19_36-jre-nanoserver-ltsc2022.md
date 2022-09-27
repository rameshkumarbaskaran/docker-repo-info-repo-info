## `eclipse-temurin:19_36-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:7030b7547dfa404625044545563817b338fedb45665cedbf0f835080db5529d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `eclipse-temurin:19_36-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:3da261c96f33edca5d7e2d8040c638fd9428b1484e358f540bc89ae314681412
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163381676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb53599cfc29b04530b5f2032c48b64bbf53ed5fa801132471df74812060894`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Mon, 26 Sep 2022 23:29:31 GMT
COPY dir:941cb8f5f97f3f5d2a48807df827e977e3ea22f3a1de758e43d87dd2ec67a41d in C:\openjdk-19 
# Mon, 26 Sep 2022 23:29:46 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:673cb7877eae23fc66e19d6c808763d26e926c59ff24e0fe146189303c2d6377`  
		Last Modified: Mon, 26 Sep 2022 23:36:00 GMT  
		Size: 45.1 MB (45102165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8b72cbd77c44a684a47ed1b937809ef47c3fd81ce9857359256fec0fa4b02e`  
		Last Modified: Mon, 26 Sep 2022 23:35:52 GMT  
		Size: 62.0 KB (62017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
