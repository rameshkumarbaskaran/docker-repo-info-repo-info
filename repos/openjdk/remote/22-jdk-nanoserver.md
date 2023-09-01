## `openjdk:22-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:50d144686686766e3d9afd85917e9477c20a7aacb31b51d7926e9e9a7fd4e8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `openjdk:22-jdk-nanoserver` - windows version 10.0.17763.4737; amd64

```console
$ docker pull openjdk@sha256:cc4083c437f902380f64040d7e328e88d128c434a17920a328cb60c4f76deb06
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.3 MB (307303562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8789a1ba91f7a84457b9145ccd08b3a6858bc81e05386a18171c10f93318ec9a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Aug 2023 08:33:47 GMT
RUN Apply image 10.0.17763.4737
# Wed, 09 Aug 2023 23:39:50 GMT
SHELL [cmd /s /c]
# Thu, 10 Aug 2023 02:42:08 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 10 Aug 2023 02:42:09 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 02:42:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 10 Aug 2023 02:42:20 GMT
USER ContainerUser
# Fri, 01 Sep 2023 01:17:58 GMT
ENV JAVA_VERSION=22-ea+13
# Fri, 01 Sep 2023 01:18:12 GMT
COPY dir:c1297b317f7c0843583653cc085803bf40ce894f37193a4a9f39a934dfe05fb6 in C:\openjdk-22 
# Fri, 01 Sep 2023 01:18:25 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 01 Sep 2023 01:18:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86fab75eb466cadf89d853682179b3b57eba9fe28c78041dd52bced81e18a627`  
		Last Modified: Tue, 08 Aug 2023 17:55:54 GMT  
		Size: 104.5 MB (104459386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7e08c5247c8c7d832882da17ac85015e9dd4d4dfc9e4114fc14746eb2abded`  
		Last Modified: Thu, 10 Aug 2023 00:21:01 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a07a6ee55409326d8105cc13d850b1705bbe4498575cf2e27bc34e78a1b5063`  
		Last Modified: Thu, 10 Aug 2023 02:50:16 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f896f4ed09b9390bcd098f89bb4624ae91e82cf7a9c4588ecdeeaa28378701`  
		Last Modified: Thu, 10 Aug 2023 02:50:15 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa6961892f2fba93ceeaf5806dc38793f041309ff787a61ccbd94e178ffd4af`  
		Last Modified: Thu, 10 Aug 2023 02:50:16 GMT  
		Size: 71.1 KB (71084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d01d10dd6ecb83bb10dfbaee0c9743aa78c0fb19d3da95691428a5cb7c9e078`  
		Last Modified: Thu, 10 Aug 2023 02:50:13 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbe6ab76f786e8921a98924d4e1808129f3b3c0f3e5976c462c7c0ed89fedcf`  
		Last Modified: Fri, 01 Sep 2023 01:21:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6613cf5e39297937695ffb73308f735d0972b2a8255229e3d9c83d665e5b96`  
		Last Modified: Fri, 01 Sep 2023 01:21:21 GMT  
		Size: 198.9 MB (198931958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a4474e808667100d5e4cc0b7bd143c39f6b19dc3b7f9ba36b016ad0c8119cf`  
		Last Modified: Fri, 01 Sep 2023 01:21:03 GMT  
		Size: 3.8 MB (3834221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e468debdebfeec1e11e4365638b96a5d8e2b7095dd08bb00f76ab156d3c9b239`  
		Last Modified: Fri, 01 Sep 2023 01:21:01 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
