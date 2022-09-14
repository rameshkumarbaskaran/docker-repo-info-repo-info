## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:8d78cd4bb54ae26c8136394b0f47fee0200f37d270bd87e72b0584852cc8af06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:8dbadea33c87f2b3ddecd2bb838049b91a7c19c1ed171cb0387005e099e7730d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310661149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83a63f857b6d898731992d4256c979feff8132deb36c7e28306832685f1e422`
-	Default Command: `["jshell"]`
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
# Wed, 14 Sep 2022 16:40:08 GMT
COPY dir:b7b3112beefc8be2dd5c6a3897a52ba756c9a344294f20db387fa022b341211c in C:\openjdk-11 
# Wed, 14 Sep 2022 16:40:24 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 14 Sep 2022 16:40:25 GMT
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
	-	`sha256:eedf8396f61e4be9f99c07d3c0b2e1f90d1404845980e1c39925057e3bf61178`  
		Last Modified: Wed, 14 Sep 2022 16:58:27 GMT  
		Size: 192.4 MB (192367898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802c3b15bc1eee061df0f6bdb8a07423aebc45eb6fde5f98daeee3ca78869a1e`  
		Last Modified: Wed, 14 Sep 2022 16:58:07 GMT  
		Size: 75.9 KB (75916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff13fd8742796c81c0752f46f499eca57149ee6ca1eaa8c4016b4a2a4f39e22`  
		Last Modified: Wed, 14 Sep 2022 16:58:08 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.17763.3406; amd64

```console
$ docker pull eclipse-temurin@sha256:7ae724af8d0f13e7374e04d9c10bc2f49c4130d1a641c82e0301c35e2943d1ef
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295854939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba804e4a550229854b66c536ca20373627191e3adb454846245efc86436f6d6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 16:03:00 GMT
SHELL [cmd /s /c]
# Wed, 14 Sep 2022 16:12:05 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 14 Sep 2022 16:12:06 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 14 Sep 2022 16:12:07 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 16:12:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Sep 2022 16:12:17 GMT
USER ContainerUser
# Wed, 14 Sep 2022 16:12:33 GMT
COPY dir:b7b3112beefc8be2dd5c6a3897a52ba756c9a344294f20db387fa022b341211c in C:\openjdk-11 
# Wed, 14 Sep 2022 16:12:46 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 14 Sep 2022 16:12:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:233f09b2a52487084f2cfb5e06dac2815651432c9d37c729582f59cfcf66b243`  
		Last Modified: Wed, 14 Sep 2022 16:47:12 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0cd1b11fcd5c6501385ccbf55adda353b30907a4f34fa696e8ba9eb57fe72`  
		Last Modified: Wed, 14 Sep 2022 16:49:51 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f53381a52e06d5ca3814b41e1c956eeeda1a756850ec94c56924987e956dd14`  
		Last Modified: Wed, 14 Sep 2022 16:49:51 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81367e02484ec9fdab571c6ad7be9463a7eb5d39a07b7d0204b16acb30e2e6af`  
		Last Modified: Wed, 14 Sep 2022 16:49:51 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56ea5adb1e9aa6a064aa275c4d5aee7b97d797faaa27b0faa4ff45d8e39bbab`  
		Last Modified: Wed, 14 Sep 2022 16:49:49 GMT  
		Size: 76.0 KB (76011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b9ea271df35fcd3360936af19dc706b939d9ed5f8894ccf26f73c1037ea461`  
		Last Modified: Wed, 14 Sep 2022 16:49:49 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc6ff87b38633f23ae16ed81904ea878ca2e01c1f2528afc475d405da68c93b`  
		Last Modified: Wed, 14 Sep 2022 16:50:08 GMT  
		Size: 192.4 MB (192369586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56480c7649f204eece068753d14fc77fe5112c01da352877875a2aca16511241`  
		Last Modified: Wed, 14 Sep 2022 16:49:49 GMT  
		Size: 68.4 KB (68369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47cdb39535beaf42095ea0d9a0745e5652ee0f9364bee376ba99b50b7e93ee5`  
		Last Modified: Wed, 14 Sep 2022 16:49:49 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
