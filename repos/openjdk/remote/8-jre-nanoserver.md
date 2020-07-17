## `openjdk:8-jre-nanoserver`

```console
$ docker pull openjdk@sha256:3f3f4b430c57ded4981911316fc8644e3d4ccf40c0c77fff2769dced4d3cccc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `openjdk:8-jre-nanoserver` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:9d1e8fe6556a51506f4a6a48d4fb0563badaca87161fec6c8d741c05f837d4ac
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138466736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc583f90fe615c02ff788cc161dbb33cbb48857b294b966695319762ca31035`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Jul 2020 13:50:07 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jul 2020 01:54:43 GMT
SHELL [cmd /s /c]
# Wed, 15 Jul 2020 02:34:08 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Jul 2020 02:34:09 GMT
USER ContainerAdministrator
# Wed, 15 Jul 2020 02:34:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 15 Jul 2020 02:34:25 GMT
USER ContainerUser
# Fri, 17 Jul 2020 00:02:22 GMT
ENV JAVA_VERSION=8u262
# Fri, 17 Jul 2020 00:16:59 GMT
COPY dir:9eeb064c358340bf4c43c46608fc234381de425bcb675b8260eb038f2fb7541d in C:\openjdk-8 
# Fri, 17 Jul 2020 00:17:12 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version
```

-	Layers:
	-	`sha256:dc95608099543221ef539391bfece5c1ce37b97af9da457f5990349cab028a12`  
		Size: 100.9 MB (100895619 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f6486e4debac36806ed3527d9b1baea75c1a807e26baccdd0a2f521c814273f`  
		Last Modified: Wed, 15 Jul 2020 02:43:55 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635f616413e2ffeb2b698529474f16b802473016d0380fd29b21f12527e7006d`  
		Last Modified: Wed, 15 Jul 2020 02:54:29 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a9bf2169040f2fa44109296c3dc79cd3e81ec224a0a19ae4d74f3866e4bac3`  
		Last Modified: Wed, 15 Jul 2020 02:54:29 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1401126acf0a8e1002c19605d846794b2a2e714f7bc1293cddc58869c1dc38c2`  
		Last Modified: Wed, 15 Jul 2020 02:54:27 GMT  
		Size: 63.8 KB (63805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f29752410c44cda8c2ee96c26c8abfed12f174fd499396fae2c94332705efa3`  
		Last Modified: Wed, 15 Jul 2020 02:54:27 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436fdde09e7b213f0e8a06317010e9a34201f40cd9880c49542f3cabce9401f0`  
		Last Modified: Fri, 17 Jul 2020 00:25:18 GMT  
		Size: 840.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c6a88170c3d6d8d007d700bc596582f615bde60d656ce8f0be88ecfad4a4f8`  
		Last Modified: Fri, 17 Jul 2020 00:26:09 GMT  
		Size: 37.4 MB (37426710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70612f30d99e7371edb87b0ccf5603dbfcaf7d6fe20e5423fced023dba18a627`  
		Last Modified: Fri, 17 Jul 2020 00:26:03 GMT  
		Size: 76.2 KB (76206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
