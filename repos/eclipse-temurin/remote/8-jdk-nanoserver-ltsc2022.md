## `eclipse-temurin:8-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:1ca97160daefac98680533bed3abb80ff37c935d9f0ee62168f2d46f887d2c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.768; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.768; amd64

```console
$ docker pull eclipse-temurin@sha256:b6b14b07af4cbe25a542c3671b7171cf02c8bcf5e246b0dcdb4e8a733f495aab
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218233922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7aaffe5000040e8b293661b95178d5ff99533c222f8f99398f21ac61de371b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jun 2022 04:10:14 GMT
RUN Apply image 10.0.20348.768
# Wed, 15 Jun 2022 18:08:52 GMT
SHELL [cmd /s /c]
# Wed, 15 Jun 2022 18:08:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Wed, 15 Jun 2022 18:08:54 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Jun 2022 18:08:55 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 18:09:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jun 2022 18:09:27 GMT
USER ContainerUser
# Wed, 15 Jun 2022 18:09:39 GMT
COPY dir:fe4a23cbc3aecb3ea1bcf0dca600117ebc14653b599151b614599054d6b82722 in C:\openjdk-8 
# Wed, 15 Jun 2022 18:09:58 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:fca88290e1b048d74ec4e9d1548c4ec09dc3921f80285f39a186278fcaf2d86f`  
		Size: 118.0 MB (117976537 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:60cbdb7704dc53714205f32082d3faa20d7c93a53c40cb88f22581e85a2943fc`  
		Last Modified: Wed, 15 Jun 2022 19:13:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b9c7257f423af50da401b2650d6841549dbd95f433b8bb78423f42558cf255`  
		Last Modified: Wed, 15 Jun 2022 19:13:51 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5306ed3ad268c7fefb13d64b3f2cd6ee35898cd2bffb428b6e1c2aa20399568b`  
		Last Modified: Wed, 15 Jun 2022 19:13:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf5d1ee027f5de50fd4b2a177fd62b473a0c007c38d86ed1aca48cdde03b8cf`  
		Last Modified: Wed, 15 Jun 2022 19:13:44 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26734ec0ceb29a842317ce27bd3cdc7fac47ba4055a0b5f3d84d283a318f0f43`  
		Last Modified: Wed, 15 Jun 2022 19:13:44 GMT  
		Size: 86.7 KB (86727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdfe0c7bc62a1f4b9cecfbc56d7f04f29a4788cfb900e246605e476ac500bff`  
		Last Modified: Wed, 15 Jun 2022 19:13:44 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e676e67ea647c4e02f4da227eca43611dd5d167c2c6a39411f6b7c78d4d2590c`  
		Last Modified: Wed, 15 Jun 2022 19:15:32 GMT  
		Size: 100.1 MB (100077122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cf59d7ff6e1a0519aa7aade92089697bcfee268d384b7157149cc8967790df`  
		Last Modified: Wed, 15 Jun 2022 19:13:44 GMT  
		Size: 87.7 KB (87695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
