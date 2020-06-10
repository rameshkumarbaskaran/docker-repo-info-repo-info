## `openjdk:8-jre-nanoserver`

```console
$ docker pull openjdk@sha256:9bb20118f4a7f524e547dde5c73b4297c7560b42d56f47380320888e932a5ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `openjdk:8-jre-nanoserver` - windows version 10.0.17763.1282; amd64

```console
$ docker pull openjdk@sha256:6fb924f403efec1000f62005acc23a0e7809f3949bf7088cb4abab9d341df19e
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138589660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfced5a47540c3bf2470ccc455b0d09f344e97c3e9cea9b1f08d0d846dbf8351`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jun 2020 11:12:32 GMT
RUN Apply image 1809-amd64
# Tue, 09 Jun 2020 22:42:44 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2020 23:10:49 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 09 Jun 2020 23:10:50 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2020 23:11:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Tue, 09 Jun 2020 23:11:03 GMT
USER ContainerUser
# Tue, 09 Jun 2020 23:11:03 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 23:15:06 GMT
COPY dir:efe8678d9be4067f8f1280960ef457f634d7198257f7398711cb683e771f08bd in C:\openjdk-8 
# Tue, 09 Jun 2020 23:15:22 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version
```

-	Layers:
	-	`sha256:c7d6d47ff7dfb2aa4d4e819641b93ec971e8541978dff0ffc24c193babeb8c07`  
		Size: 101.0 MB (101043386 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5b390ee94e41353252b153770fa99d748992b90bdaf9abf7c785d93be52ee02c`  
		Last Modified: Tue, 09 Jun 2020 23:19:14 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ceaf36f52880d38e22fe7b7f8fb469078f6c3cbd8878cb0cb6622f84331a55`  
		Last Modified: Tue, 09 Jun 2020 23:33:31 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495ef2c347d7f8951f93f5b11447092502dbf5148e0afc42bd6a93cdfac22e43`  
		Last Modified: Tue, 09 Jun 2020 23:33:31 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c5b466a2d08cf215a8f231507f418d6f8f0937fd9ea6be0f9eba83d332301b`  
		Last Modified: Tue, 09 Jun 2020 23:33:29 GMT  
		Size: 69.0 KB (69041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73c238f787394408ba51a1bb4103d83b74626d53a8c138fcd934fe665c57589`  
		Last Modified: Tue, 09 Jun 2020 23:33:29 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8c25bbf35b268fa8cdd03b4ded93b7063f5895c399f1c52dccaf183abc295e`  
		Last Modified: Tue, 09 Jun 2020 23:33:28 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695e4521cb5eaf2847038a7af2cd0ace4d604b586a17a77d853895cb60d7047f`  
		Last Modified: Tue, 09 Jun 2020 23:35:10 GMT  
		Size: 37.4 MB (37420833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433120e8f5347f0a6bfec4b5a19ac82410ab11265fcca3200c2f35241fec2956`  
		Last Modified: Tue, 09 Jun 2020 23:35:04 GMT  
		Size: 52.0 KB (52040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
