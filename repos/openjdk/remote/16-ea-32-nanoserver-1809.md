## `openjdk:16-ea-32-nanoserver-1809`

```console
$ docker pull openjdk@sha256:720e03381122cadf693cd171a74297b9ccd2bd5243d50f09c84fe015a75e3085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:16-ea-32-nanoserver-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:4063dc60ce255223af8e0658b8dcb8d9ca71676f1d9c8e6bf6dab914de4383ff
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285117168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b62a2af60710b7e3e6049af498c5e845c7e69dccf5c6d1a287759ed0dfc530`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:56:48 GMT
SHELL [cmd /s /c]
# Wed, 13 Jan 2021 20:35:00 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 13 Jan 2021 20:35:01 GMT
USER ContainerAdministrator
# Wed, 13 Jan 2021 20:35:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 13 Jan 2021 20:35:14 GMT
USER ContainerUser
# Fri, 15 Jan 2021 23:27:34 GMT
ENV JAVA_VERSION=16-ea+32
# Fri, 15 Jan 2021 23:27:59 GMT
COPY dir:a25b1849e7d9efb391419f421e3babb9446a99dea41600994e998ce311f17996 in C:\openjdk-16 
# Fri, 15 Jan 2021 23:28:25 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 15 Jan 2021 23:28:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c2b6c001c337f812bceb3b03d15a70d1d9905540658e751e42f20f7cc0ddc819`  
		Last Modified: Wed, 13 Jan 2021 21:16:47 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22f53d1f631e14bb9677766dc089ce4caf4dae9627d1513773cfff289e94f42`  
		Last Modified: Wed, 13 Jan 2021 21:19:22 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43af010a68e2978961a3d63887efbc1230811009f66bd683e9fc4174f4185177`  
		Last Modified: Wed, 13 Jan 2021 21:19:20 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3132f9cb979d43ab9de9d926bc492cf9bd38763c7e557f278fe358ac557f14b6`  
		Last Modified: Wed, 13 Jan 2021 21:19:19 GMT  
		Size: 65.1 KB (65097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d6c42dd2fabc75c92d7f5ad83fa610805a5e5dea3aba8da7ef9c4271f5ec93`  
		Last Modified: Wed, 13 Jan 2021 21:19:16 GMT  
		Size: 937.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5111055bff0eee34a81bafca4a8b4796f0ca1c890ca1d468888cc778bef3c039`  
		Last Modified: Fri, 15 Jan 2021 23:39:00 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5ec72437c1ab85810c93141228262df1b466efb83d07a2e7026799a3455620`  
		Last Modified: Fri, 15 Jan 2021 23:39:20 GMT  
		Size: 180.0 MB (180031247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d867b860a3243be54b47093fb4fb81233fe17a8e5cde9e622aabd807b7763f16`  
		Last Modified: Fri, 15 Jan 2021 23:39:01 GMT  
		Size: 3.7 MB (3674905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867070a3676c688d11617577d9e00c65a120f5f2267fc5a588df503764087ae6`  
		Last Modified: Fri, 15 Jan 2021 23:38:59 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
