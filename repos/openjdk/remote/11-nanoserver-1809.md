## `openjdk:11-nanoserver-1809`

```console
$ docker pull openjdk@sha256:822d524ea8594a5dc08a6ae1b547b7e78aa71b1743ddf3b0db359a0ef3c6e286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `openjdk:11-nanoserver-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull openjdk@sha256:d830e1365379d8b2ebde586429a42b6614530e66edb7460589c50b288790850f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.0 MB (293979847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9a24ac047dd0c172915ce05a814714ff065e8b0b5e95a9adccc1e90cde8c0f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 00:38:23 GMT
SHELL [cmd /s /c]
# Wed, 15 Sep 2021 00:55:13 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 15 Sep 2021 00:55:15 GMT
USER ContainerAdministrator
# Wed, 15 Sep 2021 00:55:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 15 Sep 2021 00:55:25 GMT
USER ContainerUser
# Wed, 15 Sep 2021 00:55:25 GMT
ENV JAVA_VERSION=11.0.12
# Wed, 15 Sep 2021 00:55:43 GMT
COPY dir:8d687b3cc71690b95b3812413f66d278c1566215f055e8d2ed9ac022b638e9a3 in C:\openjdk-11 
# Wed, 15 Sep 2021 00:55:55 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 15 Sep 2021 00:55:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:807d06303c39b2317729754a4c7ad6501e59c16ee464f8f671f9947774f62f72`  
		Last Modified: Wed, 15 Sep 2021 01:10:56 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0639065e91c96957c253786d29acecc097be0f834bfa29a80fe20459de5baf48`  
		Last Modified: Wed, 15 Sep 2021 01:25:15 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b48314eb9be42d9287b4e3d4ce718916e4b80f91f4acbf24787b3606b738bc9`  
		Last Modified: Wed, 15 Sep 2021 01:25:15 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e21f3f3ff19767c148ef15716649791cc7daaa79830a467d7364cbea66d876`  
		Last Modified: Wed, 15 Sep 2021 01:25:15 GMT  
		Size: 72.5 KB (72517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374a4285b55f399ddb1d4dd19ea5c2f893907fdd3dc1737b6cf60fc97dafc5ec`  
		Last Modified: Wed, 15 Sep 2021 01:25:13 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8219361b61e0db6e644f5041c32c009b35865acf53950161eb6f2d621f57a874`  
		Last Modified: Wed, 15 Sep 2021 01:25:12 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15429843cbc56510cc751adbac425f645bf29b027d6d1cca9857a164259654d6`  
		Last Modified: Wed, 15 Sep 2021 01:25:29 GMT  
		Size: 191.2 MB (191151012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a37b5e933c5d278ae7356428ffc86c3a14fc05828c757c39491fe695d156f0`  
		Last Modified: Wed, 15 Sep 2021 01:25:13 GMT  
		Size: 46.2 KB (46225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9392ddba82a5b2efe9a70cf4bd207d8b8997a3f9ea51c8794a9f90a848cdbe39`  
		Last Modified: Wed, 15 Sep 2021 01:25:12 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
