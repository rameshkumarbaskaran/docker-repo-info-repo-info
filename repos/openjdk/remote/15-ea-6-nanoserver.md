## `openjdk:15-ea-6-nanoserver`

```console
$ docker pull openjdk@sha256:4f7ea374548c65aafa431fe981ebe95faa6402f26d5640e9f8f22b2651eeb2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `openjdk:15-ea-6-nanoserver` - windows version 10.0.17763.973; amd64

```console
$ docker pull openjdk@sha256:66ca66e808706701836caff40304e10edb7bb80634baafa11ea7e5c8a4bb9214
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298526916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402d0dad0423c7735aaf68e9e2e57d9fe1586ab023674813501163cfdb8cf24e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Tue, 14 Jan 2020 23:56:11 GMT
SHELL [cmd /s /c]
# Tue, 14 Jan 2020 23:56:12 GMT
ENV JAVA_HOME=C:\openjdk-15
# Tue, 14 Jan 2020 23:56:13 GMT
USER ContainerAdministrator
# Tue, 14 Jan 2020 23:56:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Tue, 14 Jan 2020 23:56:31 GMT
USER ContainerUser
# Sat, 18 Jan 2020 00:22:05 GMT
ENV JAVA_VERSION=15-ea+6
# Sat, 18 Jan 2020 00:23:07 GMT
COPY dir:c5fd4f72809bfb9ce8019dd64eba92ca8c9bc74b422944c4e4b34a80329539bc in C:\openjdk-15 
# Sat, 18 Jan 2020 00:23:36 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Sat, 18 Jan 2020 00:23:37 GMT
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
	-	`sha256:4f193e511d66e393e8623d9efd86f48f82cc15ceb19ee3a6ac9da7343da044ad`  
		Last Modified: Wed, 15 Jan 2020 01:51:04 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fab357b0406f3be040eca20b497e3bdd7e731b95865fbfbe83acf826248583`  
		Last Modified: Wed, 15 Jan 2020 01:51:03 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fed5c1fef1ff77da19cbdb310981f89c791b7c4206a8b99d9a1f114b6a5a107`  
		Last Modified: Wed, 15 Jan 2020 01:51:03 GMT  
		Size: 70.0 KB (69974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dae8d73c31bd6bb443dd054e2ff7514c3f89f2252ad8f45b02d272a63de3194`  
		Last Modified: Wed, 15 Jan 2020 01:51:01 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de8a363d47578e4e0a7d5f300978a1fc64a9c02a795523b7de56a0e9e593491`  
		Last Modified: Sat, 18 Jan 2020 00:37:22 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13d74fd77cc1aacb2df8e5faf0ea423bf0a669a9ec96d7f3ba1e322940719cd`  
		Last Modified: Sat, 18 Jan 2020 00:40:49 GMT  
		Size: 194.0 MB (193951792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c8ded2fafaa80b187ff3f16ad6e06d89eee2968a2589c91a391f16ebaf28d2`  
		Last Modified: Sat, 18 Jan 2020 00:37:24 GMT  
		Size: 3.4 MB (3445240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60664136fff479428c0ae96fca0e0ff8fbc59a5e6e95aa00ef800d98698b4c5c`  
		Last Modified: Sat, 18 Jan 2020 00:37:22 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
