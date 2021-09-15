## `openjdk:8-jre-nanoserver`

```console
$ docker pull openjdk@sha256:851a071de7de6be3afd7ee00b27ffc5234e9c26cea40ff2884a5f8a6732c784c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `openjdk:8-jre-nanoserver` - windows version 10.0.17763.2183; amd64

```console
$ docker pull openjdk@sha256:466164ee1575c1b196a316fc8cf79f5a747480264510a5ec3e926bf074a5308e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141058083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f598ef2617fa7e5f03f9848ec1503025c862539871031dca42721610489c481b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 00:38:23 GMT
SHELL [cmd /s /c]
# Wed, 15 Sep 2021 01:03:44 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Sep 2021 01:03:45 GMT
USER ContainerAdministrator
# Wed, 15 Sep 2021 01:03:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 15 Sep 2021 01:03:53 GMT
USER ContainerUser
# Wed, 15 Sep 2021 01:03:54 GMT
ENV JAVA_VERSION=8u302
# Wed, 15 Sep 2021 01:06:54 GMT
COPY dir:58006f68c4ea109e560c76de14918bddd55bac9724011203b6cdeb031fa20971 in C:\openjdk-8 
# Wed, 15 Sep 2021 01:07:03 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:807d06303c39b2317729754a4c7ad6501e59c16ee464f8f671f9947774f62f72`  
		Last Modified: Wed, 15 Sep 2021 01:10:56 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599e1258c31953f5f847484fb4c37a5bbc5b30a8a1555a7df2c1ff0e68b8ab93`  
		Last Modified: Wed, 15 Sep 2021 01:27:41 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed51cbf293591feeb6061aad188ab2cd41ac2d2f2e8c3a6858f8d6ba5377879`  
		Last Modified: Wed, 15 Sep 2021 01:27:41 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108d571bf68a07dc3c753512d7c1a67976307f9b650af9346719c4f62e41978d`  
		Last Modified: Wed, 15 Sep 2021 01:27:39 GMT  
		Size: 75.1 KB (75110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bf35bf6b36e006f9f20bf2f357cf98aff5bb2f66714383e0bd8394e9b32ca8`  
		Last Modified: Wed, 15 Sep 2021 01:27:38 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881fd4df3e13c64dc1cf1e7681e90e5cc0755381eaecc694d370ba343f271fa7`  
		Last Modified: Wed, 15 Sep 2021 01:27:38 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bab23112bf7c22ccdf98cf34314b2279f0ba01fcac043f246503bfdb926a2e1`  
		Last Modified: Wed, 15 Sep 2021 01:29:15 GMT  
		Size: 38.2 MB (38225419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3088ad82ea57b55fe8963f82542074cf59c1d5fc385a4357a7458f6666ab98`  
		Last Modified: Wed, 15 Sep 2021 01:29:10 GMT  
		Size: 48.5 KB (48505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
