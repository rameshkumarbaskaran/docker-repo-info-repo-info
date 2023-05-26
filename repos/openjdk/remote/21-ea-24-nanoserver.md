## `openjdk:21-ea-24-nanoserver`

```console
$ docker pull openjdk@sha256:09133d144ddb52fb473eb3717620155cbd1875225e4fbce7aa18b501283185f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `openjdk:21-ea-24-nanoserver` - windows version 10.0.17763.4377; amd64

```console
$ docker pull openjdk@sha256:d0bef9bd2f0de298d3967321ab9dfd7133208fa887081889ef825079f75c672a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305586593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc7cd6d01f9cc16840783267fa25950ff5e8e960afa85648847fbd77b57c9a6`
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
# Fri, 26 May 2023 00:18:18 GMT
ENV JAVA_VERSION=21-ea+24
# Fri, 26 May 2023 00:18:33 GMT
COPY dir:f0c6b399cb66ad20ceda72050177b2f8e67336a728e132cbef6a12b589f9d529 in C:\openjdk-21 
# Fri, 26 May 2023 00:18:47 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 26 May 2023 00:18:48 GMT
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
	-	`sha256:4d07158dceef8b39779a4ef551d9495c1ebbd073260c06c18d7579d77a305711`  
		Last Modified: Fri, 26 May 2023 00:20:52 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d23e4e177fbeb515c5a6001d600410d1c3f6619ca76c06d831272278b7dd6d9`  
		Last Modified: Fri, 26 May 2023 00:21:12 GMT  
		Size: 197.3 MB (197328258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9d6d14935294b79c4139cea40f7539dd18104e2253c4b29d9d28149b967eda`  
		Last Modified: Fri, 26 May 2023 00:20:53 GMT  
		Size: 3.8 MB (3800497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df85469c10bee51eb9204b378fa61ea6245dab0fe4cb71fd949a469d9bcc9e69`  
		Last Modified: Fri, 26 May 2023 00:20:52 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
