## `openjdk:19-nanoserver`

```console
$ docker pull openjdk@sha256:df8cca894327dbc185c3847b431f2fa41f3d33cb8f72849514e7af6fc7ced2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `openjdk:19-nanoserver` - windows version 10.0.17763.2366; amd64

```console
$ docker pull openjdk@sha256:dfde5781c17ed54662804808bcae362dc740b0c142c1c37d2422c17dfdaba96e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291318003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff76639e8de8ddb3cd33ecc1c5770cca8798d32d85c18a8d0db6e8bd081e008`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 05:18:44 GMT
SHELL [cmd /s /c]
# Sat, 18 Dec 2021 07:02:53 GMT
ENV JAVA_HOME=C:\openjdk-19
# Sat, 18 Dec 2021 07:02:54 GMT
USER ContainerAdministrator
# Sat, 18 Dec 2021 07:03:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 18 Dec 2021 07:03:07 GMT
USER ContainerUser
# Mon, 27 Dec 2021 19:06:02 GMT
ENV JAVA_VERSION=19-ea+3
# Mon, 27 Dec 2021 19:06:35 GMT
COPY dir:748284eb63c023af6d44703d022c2297b66561fd7bea617827b8be3e1ce3039b in C:\openjdk-19 
# Mon, 27 Dec 2021 19:06:53 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 27 Dec 2021 19:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4c557aac927613dd487d7c04b01a8eeb8ad174693f61b14c8f4285f1db6afdd2`  
		Last Modified: Sat, 18 Dec 2021 06:13:05 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee77840953b5908197d8833c877fc68713477ba9d823d0917d99682670f0a3f`  
		Last Modified: Sat, 18 Dec 2021 10:56:34 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0e4c6e5345c964ccca26a0985b4ee9da30d0ef03b76b305170b194938512c6`  
		Last Modified: Sat, 18 Dec 2021 10:56:34 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed1fe46a03128a021a9357486f07c8e6f1d8237ed48f484797f70e45efcc27b`  
		Last Modified: Sat, 18 Dec 2021 10:56:33 GMT  
		Size: 67.4 KB (67397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0a3a92f853e640905ade39909c46ce2b476df94464a7649628a0d6a22118db`  
		Last Modified: Sat, 18 Dec 2021 10:56:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8a20f77da0525e4f408a1af18a74a171fbf6e67092a0c17d296f2eaef475ba`  
		Last Modified: Mon, 27 Dec 2021 20:26:12 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219d700bb9f49119c097df657a68645863982356445c3ded46394db958a11cdc`  
		Last Modified: Mon, 27 Dec 2021 20:26:32 GMT  
		Size: 184.8 MB (184784482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f4880d9ee3a6aafd1a7f6c033a5c7e5053d4fa3b720e2148d8e1d8e17407e3`  
		Last Modified: Mon, 27 Dec 2021 20:26:14 GMT  
		Size: 3.6 MB (3555095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494ed9180522c12ecb7db8a6afb58f07db287ba22d1536a940193638e77c20c6`  
		Last Modified: Mon, 27 Dec 2021 20:26:13 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
