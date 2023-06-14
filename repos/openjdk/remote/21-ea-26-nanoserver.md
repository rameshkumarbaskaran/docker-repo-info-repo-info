## `openjdk:21-ea-26-nanoserver`

```console
$ docker pull openjdk@sha256:ab4e2203df51596f5f67ce8a291af71bdc72da6815cbb6d4dffb05f29de69973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `openjdk:21-ea-26-nanoserver` - windows version 10.0.17763.4499; amd64

```console
$ docker pull openjdk@sha256:91ee84741af7f94d7a7914ae3afe4ae95dd95351064378f19d3ee61337e6a59a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 MB (306237564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abd3d1247efb45be85495fb55b22f7af0e650da55ad1aa9098456c10ef4ac3c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jun 2023 12:28:32 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 17:41:42 GMT
SHELL [cmd /s /c]
# Wed, 14 Jun 2023 20:32:10 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 14 Jun 2023 20:32:11 GMT
USER ContainerAdministrator
# Wed, 14 Jun 2023 20:32:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Jun 2023 20:32:21 GMT
USER ContainerUser
# Wed, 14 Jun 2023 20:32:21 GMT
ENV JAVA_VERSION=21-ea+26
# Wed, 14 Jun 2023 20:32:35 GMT
COPY dir:ca6175116d2a12ef23a44ba1f6a31c07fd45a0edd19a1cdd3d8b538a6e52dd6c in C:\openjdk-21 
# Wed, 14 Jun 2023 20:32:49 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 14 Jun 2023 20:32:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:234d39d9b188e7f36d5a77b0d54990ea826551314b6703c83aef3ef20b1a7050`  
		Last Modified: Tue, 13 Jun 2023 19:06:23 GMT  
		Size: 104.4 MB (104397895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2364e413270ecc5b57d2596b092fb57b828229b59e810d9f345fc0d31ca535d`  
		Last Modified: Wed, 14 Jun 2023 18:26:46 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c86c8f72d5c620385f29493830932257c53d9dad74802ecdf0bdbc03b2494c`  
		Last Modified: Wed, 14 Jun 2023 20:37:08 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30698f58bfeb99d6b9b76177da8956540b4b318293543c1e5c8447403dc97f1`  
		Last Modified: Wed, 14 Jun 2023 20:37:08 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c50e91142bca7a5ff55e1ebc6fd6e7a26cdfc9d0890ad2eb8a5c7b031598294`  
		Last Modified: Wed, 14 Jun 2023 20:37:08 GMT  
		Size: 68.8 KB (68836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a22e7e5b49f87fd9c56f26a1e630fdf989e0f48edc7f35e074d47642e4af389`  
		Last Modified: Wed, 14 Jun 2023 20:37:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1c308f4712f2a3f87df55fba6467ee79cb7b69a362fb5002422687dac80092`  
		Last Modified: Wed, 14 Jun 2023 20:37:07 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f36f675af765fb5d9d76254cad36ecef973dc500e203ada667a0ee9ba32568`  
		Last Modified: Wed, 14 Jun 2023 20:37:26 GMT  
		Size: 197.9 MB (197944931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df447e17a7f8c3400328318b8a3650e16434edc0ca5163f35eedc88a9106a76f`  
		Last Modified: Wed, 14 Jun 2023 20:37:08 GMT  
		Size: 3.8 MB (3818907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4973f06117295c71b5524793cc9262048fc3d9a29dc18fc73e7b126a661b2d`  
		Last Modified: Wed, 14 Jun 2023 20:37:06 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
