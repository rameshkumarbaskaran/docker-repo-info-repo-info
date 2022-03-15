## `openjdk:19-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:e4bd9c23329edf6253394b7ce016a20ed72ae706638ef2641b4dc4d7a427883f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `openjdk:19-ea-jdk-nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull openjdk@sha256:69046a4171d56283a744319a2a11ea6b7791343b76786b236363cf3c6df35bf7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294490353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2641dec2dba4173f35a1744b8592552afcaf756b768cc3065ca55d4bb1931408`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Tue, 08 Mar 2022 21:56:20 GMT
SHELL [cmd /s /c]
# Wed, 09 Mar 2022 17:13:35 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 09 Mar 2022 17:13:36 GMT
USER ContainerAdministrator
# Wed, 09 Mar 2022 17:13:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Mar 2022 17:13:48 GMT
USER ContainerUser
# Mon, 14 Mar 2022 19:17:31 GMT
ENV JAVA_VERSION=19-ea+13
# Mon, 14 Mar 2022 19:17:45 GMT
COPY dir:209726380494b64e9436ae0708c25e6ead279a342e2cc4a1c80063a11b5f805c in C:\openjdk-19 
# Mon, 14 Mar 2022 19:18:06 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 14 Mar 2022 19:18:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e0065cd23a657c8f30ae5af121fd18451d2307835a1124ea57c80683eda26c94`  
		Last Modified: Tue, 08 Mar 2022 22:37:21 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab71e137ca33aa5127b0e55796dd1ffba9bdcf004bd9e37533e42daa5ebd2bf`  
		Last Modified: Wed, 09 Mar 2022 17:42:19 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b9123b1e06063521bbaeb5ac4dc7ac8960be154774560ca5c9db99a43b2d8d`  
		Last Modified: Wed, 09 Mar 2022 17:42:19 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ab23123853d0353a546935f5a1d10d91f5c5c44d79bf888ae0d353941c6938`  
		Last Modified: Wed, 09 Mar 2022 17:42:19 GMT  
		Size: 68.0 KB (68002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e219e794e6ab490d19f1491c0d2de445c430aac5eceb51f362b916de14e9250d`  
		Last Modified: Wed, 09 Mar 2022 17:42:17 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955c2873c308c1e3bc44fefeb7335057ee817c1ce2549368d98879ddcdf07dc3`  
		Last Modified: Mon, 14 Mar 2022 20:21:29 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16f797f36881a5c0a31f0ff8303030716e92a7e246afe05a8ff41829e91f8e6`  
		Last Modified: Mon, 14 Mar 2022 20:24:46 GMT  
		Size: 187.8 MB (187796475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e390b902f23440065ae1dbd5043829e209c4318bcd8343adec391e9aac176ab3`  
		Last Modified: Mon, 14 Mar 2022 20:21:33 GMT  
		Size: 3.6 MB (3564409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea575e4b577e182f4548fa30e09c10242bb66d92fb374b98bfdc57dac26d0db9`  
		Last Modified: Mon, 14 Mar 2022 20:21:29 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
