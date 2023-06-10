## `openjdk:21-ea-26-nanoserver-1809`

```console
$ docker pull openjdk@sha256:f0423c403dd85b1b7336e5421f7d997d79d97c11e6c3c0f2d98e21b0d1a3024a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `openjdk:21-ea-26-nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull openjdk@sha256:3ff26439cdf2d078ab822385a3aff3bdf624c43e71acb909f0aec0c81ff4c98c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 MB (306198787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd83feffff7ee1c34b48edaf77b7f0d802f791044e3e12a55e752f0ebe65d65`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 00:40:01 GMT
SHELL [cmd /s /c]
# Wed, 10 May 2023 02:57:56 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 May 2023 02:57:56 GMT
USER ContainerAdministrator
# Wed, 10 May 2023 02:58:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 May 2023 02:58:09 GMT
USER ContainerUser
# Sat, 10 Jun 2023 00:18:17 GMT
ENV JAVA_VERSION=21-ea+26
# Sat, 10 Jun 2023 00:18:33 GMT
COPY dir:ca6175116d2a12ef23a44ba1f6a31c07fd45a0edd19a1cdd3d8b538a6e52dd6c in C:\openjdk-21 
# Sat, 10 Jun 2023 00:18:47 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 10 Jun 2023 00:18:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b79dd15c5dd82bc10521b9a4e49241f70088bc6edbb286f90be198abea55e23`  
		Last Modified: Wed, 10 May 2023 03:01:27 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40d6657961af59b636be2db4aa1fcef304eb245271a8ae41504adce8615cd1d`  
		Last Modified: Wed, 10 May 2023 03:01:26 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f906b9562d5b2a03bb6c35a1ad6ee0d9becffcc133bb4d938b390c69e08ed9ed`  
		Last Modified: Wed, 10 May 2023 03:01:26 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa4992dcb0ef11fcada4b2f46b4a9c8cde731d43e793119cd32bd5fed253cd8`  
		Last Modified: Wed, 10 May 2023 03:01:26 GMT  
		Size: 66.9 KB (66929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee642db739fb63532d81702ffb8160c34a27c60b4725dcea8a48eae94769a63`  
		Last Modified: Wed, 10 May 2023 03:01:24 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39320e7243ec7db66b0b0027bc6982d87f418812a4936d8a6df69b07797c23b`  
		Last Modified: Sat, 10 Jun 2023 00:20:48 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54e81f1b655b2c6c32d845af72d32a48ac30583f678128939a3445ff475736e`  
		Last Modified: Sat, 10 Jun 2023 00:21:08 GMT  
		Size: 197.9 MB (197940373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4c4f49f830929628f1b28d949c73f3e102c3ab159053b9b96409e5c0ab02d5`  
		Last Modified: Sat, 10 Jun 2023 00:20:49 GMT  
		Size: 3.8 MB (3800520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c0d1d1f71b165a7f9fcde801f4cc8bc1d8d2d3acbf9af3f292222eab789d47`  
		Last Modified: Sat, 10 Jun 2023 00:20:48 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
