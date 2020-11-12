## `openjdk:8u275-jre-nanoserver`

```console
$ docker pull openjdk@sha256:082e9d10a3509e35248685ee779725226a3d84ceef7617bfdbccbff59e682b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `openjdk:8u275-jre-nanoserver` - windows version 10.0.17763.1577; amd64

```console
$ docker pull openjdk@sha256:488d0069dd1fa4a47246028c32bb09a254390b8ac2ebdd0b4780ed475b6765d7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139597865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5c47548d56953bfd877d11ebd23dbe2d9b280f51267f3246f30298a4e5ac2e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:53:16 GMT
SHELL [cmd /s /c]
# Wed, 11 Nov 2020 18:19:07 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 11 Nov 2020 18:19:08 GMT
USER ContainerAdministrator
# Wed, 11 Nov 2020 18:19:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 11 Nov 2020 18:19:19 GMT
USER ContainerUser
# Thu, 12 Nov 2020 01:38:13 GMT
ENV JAVA_VERSION=8u275
# Thu, 12 Nov 2020 01:41:58 GMT
COPY dir:9c574feda3d434860f596ed9945da2b2916773d80cfb9282fa700c98a8998c43 in C:\openjdk-8 
# Thu, 12 Nov 2020 01:42:16 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:41b7be9dc08821cf81d29b16e0df54f7f3e3aeaa6407f43520c6259f2d84b10c`  
		Last Modified: Wed, 11 Nov 2020 18:27:27 GMT  
		Size: 864.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5293ca96aa254135b70635ee048740d1a51f05e657d122eecbe31de2f03f476f`  
		Last Modified: Wed, 11 Nov 2020 18:40:08 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de4cd2f1948cfa64e2c85180f38d5b346ab75f64984579c353871c117e54200`  
		Last Modified: Wed, 11 Nov 2020 18:40:07 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68eb57f2f9c7bbec6e6dab23eeb8c07223ac79ccfe78fffdfe5f3e28de0373ad`  
		Last Modified: Wed, 11 Nov 2020 18:40:04 GMT  
		Size: 67.6 KB (67580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d6560cbbc5021992b82fe5be8aed78e5e07d433aab28cc63b880d521249767`  
		Last Modified: Wed, 11 Nov 2020 18:40:05 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de579fb96f879ee3639f14281cb11dc1a986451a8bba0fac1cb7f18ee1ac092`  
		Last Modified: Thu, 12 Nov 2020 01:58:14 GMT  
		Size: 864.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8432253cbcdbe81a5604082882d9b33e82f7c61e91f434c329a9e55d21130811`  
		Last Modified: Thu, 12 Nov 2020 02:01:58 GMT  
		Size: 38.2 MB (38191009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37851d8ea950ed6b2a30d983eece9bda39b6079ddd3df14609b9a1981534801b`  
		Last Modified: Thu, 12 Nov 2020 02:01:03 GMT  
		Size: 55.2 KB (55247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
