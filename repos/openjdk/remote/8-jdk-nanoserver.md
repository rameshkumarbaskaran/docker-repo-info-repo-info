## `openjdk:8-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:eea52fe34302ab64fa02b6337e68cbf165dadf1b8695e24c345a1cc7e08bcd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `openjdk:8-jdk-nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull openjdk@sha256:32847f3acba7486fa2e49131a7b15d899a87fb42591aa7e7cb6a15584e235ae7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.3 MB (204289396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb8946ebf88ef2126ee32133d28c3d730270f425dc491be71bfb6cbb7a4fc92`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Tue, 08 Mar 2022 21:56:20 GMT
SHELL [cmd /s /c]
# Wed, 09 Mar 2022 17:35:05 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Mar 2022 17:35:06 GMT
USER ContainerAdministrator
# Wed, 09 Mar 2022 17:35:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Mar 2022 17:35:16 GMT
USER ContainerUser
# Wed, 09 Mar 2022 17:35:16 GMT
ENV JAVA_VERSION=8u322
# Wed, 09 Mar 2022 17:35:30 GMT
COPY dir:70b73c62c79b1e3a83236c8add186d48955c92966a80012af2e52ff572318d7b in C:\openjdk-8 
# Wed, 09 Mar 2022 17:35:52 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e0065cd23a657c8f30ae5af121fd18451d2307835a1124ea57c80683eda26c94`  
		Last Modified: Tue, 08 Mar 2022 22:37:21 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cae2b05f4b79e8fd3e173be31895e963d84f0cb359b7af88517005f3b2551c`  
		Last Modified: Wed, 09 Mar 2022 18:03:38 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f76aeda459522891ce5c09a14366ca6902544816234ddde267328c41ab6087`  
		Last Modified: Wed, 09 Mar 2022 18:03:38 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec184a8d491152de6c27a01be4a1aa687f007739313ba102635ef2a88f0fed22`  
		Last Modified: Wed, 09 Mar 2022 18:03:35 GMT  
		Size: 75.3 KB (75338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3244cd8eccd07203a24408e2adf77c5e0618c7f913e885d4f4b61f5f69926236`  
		Last Modified: Wed, 09 Mar 2022 18:03:35 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4724555dee6074a8f06014d9747a1321cdc874da9f0c383590a10b934966d`  
		Last Modified: Wed, 09 Mar 2022 18:03:35 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5892f8972eb4a67eb24dc593b7a0a6ae008d94b398087caa75cc2be10609b085`  
		Last Modified: Wed, 09 Mar 2022 18:03:49 GMT  
		Size: 101.1 MB (101105654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378001fcb38604a87109677c935ae207d476cdb2bf41729e9dc788d8a94cebb`  
		Last Modified: Wed, 09 Mar 2022 18:03:35 GMT  
		Size: 48.1 KB (48095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
