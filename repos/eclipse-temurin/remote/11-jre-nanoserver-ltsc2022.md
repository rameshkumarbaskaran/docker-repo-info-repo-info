## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0ef63eb4bd758b216c16596ae9c99cedcce9ac4467b81e64dca071fc0616ab20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:8d3edd37ec8662fbdcd34f0d3191b7a43c3b602f934ebe57ee59d248326f8468
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161192303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f733f778c6c9000a61b684974491d23afedae8e126be8c8b1cd1d69b37fd3b60`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Sep 2022 20:11:22 GMT
RUN Apply image 10.0.20348.1006
# Wed, 14 Sep 2022 16:38:20 GMT
SHELL [cmd /s /c]
# Wed, 14 Sep 2022 16:39:41 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 14 Sep 2022 16:39:42 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 14 Sep 2022 16:39:42 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 16:39:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Sep 2022 16:39:53 GMT
USER ContainerUser
# Wed, 14 Sep 2022 16:40:41 GMT
COPY dir:b650de7fc0e3b0755f26a7348890f8f5a4e1b6ed07c2d2df82fc07e7eb59e165 in C:\openjdk-11 
# Wed, 14 Sep 2022 16:40:54 GMT
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
	-	`sha256:69e9874cfb1290b2d18c9beffbfd99b9d1e09f8af04b374db214974968038e3e`  
		Last Modified: Wed, 14 Sep 2022 16:58:10 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ec2fe2f33ab50e9fa4932ea36425b3d16e951341beb15e4b1c762c87b2f44f`  
		Last Modified: Wed, 14 Sep 2022 16:58:10 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b9290f6a2ecdeccefa5fc537a9bad68e44802e0418c0db24ac05d1db414386`  
		Last Modified: Wed, 14 Sep 2022 16:58:10 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f528201d81349fe0b28a43ec78fab2f3b0735cdd9cfa89dc61faf9c8799738`  
		Last Modified: Wed, 14 Sep 2022 16:58:07 GMT  
		Size: 79.8 KB (79762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3285b65edefe11e2a40bacbc70c3cc99083205447f036f436c4aabdb3b0b169a`  
		Last Modified: Wed, 14 Sep 2022 16:58:07 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be1e89da0ea6c27e50f9e2a0f3f9141077e0a247a7ba3b46c7c7e3a5555b37`  
		Last Modified: Wed, 14 Sep 2022 16:58:47 GMT  
		Size: 42.9 MB (42913905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f3991beceb88a8a035e82fe4eafb6f5020abe075d9d8cbabe002acf23de075`  
		Last Modified: Wed, 14 Sep 2022 16:58:40 GMT  
		Size: 62.1 KB (62087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
