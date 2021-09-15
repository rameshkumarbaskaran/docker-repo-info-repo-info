## `openjdk:11-jre-nanoserver`

```console
$ docker pull openjdk@sha256:a52be8a47496a05bab820b5ed7e1910f823727f1790c757548c9636cd5fbd8e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `openjdk:11-jre-nanoserver` - windows version 10.0.17763.2183; amd64

```console
$ docker pull openjdk@sha256:b532c18a40ce7a99b19b46aeaef12bf3c94cf01745943e916d840845253c2e45
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142304632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4d53ca48e7814ff2d98feba7ab1b9a0af612e2c2734bf44ed3c497945ab65a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 15 Sep 2021 00:58:36 GMT
COPY dir:cfe6877c6b81ca46843a524b803b574bd01e43f05b821b8b183eb47cd476c286 in C:\openjdk-11 
# Wed, 15 Sep 2021 00:58:46 GMT
RUN echo Verifying install ... 	&& echo   java --version && java --version 	&& echo Complete.
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
	-	`sha256:b97f579563b3ec5769f45b55c8daa99552011f3d9af7feebe868ba6fb0ccb012`  
		Last Modified: Wed, 15 Sep 2021 01:26:35 GMT  
		Size: 39.5 MB (39476759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de316e293810b61ed0f6d81651b3162a4cd1b5b46a415d2f8fbbc5ae90b099fd`  
		Last Modified: Wed, 15 Sep 2021 01:26:29 GMT  
		Size: 46.3 KB (46296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
