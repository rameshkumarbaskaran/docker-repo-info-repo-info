## `openjdk:16-nanoserver-1809`

```console
$ docker pull openjdk@sha256:08646621a0ea4847ead601145a4adef0147ef6769c52a54d13830deafdd5f5a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `openjdk:16-nanoserver-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull openjdk@sha256:4a596a91f16035efaea2fcbbaaa26a8c05987fea34dd8f7cc83c709426cc0357
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (297016571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:158df221b4654c4ae51a5ee4216f8eaf792c029cc63416551aef0b3fce9d43f5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Sep 2020 12:08:18 GMT
RUN Apply image 1809-amd64
# Tue, 08 Sep 2020 20:13:38 GMT
SHELL [cmd /s /c]
# Tue, 08 Sep 2020 20:13:38 GMT
ENV JAVA_HOME=C:\openjdk-16
# Tue, 08 Sep 2020 20:13:39 GMT
USER ContainerAdministrator
# Tue, 08 Sep 2020 20:13:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Tue, 08 Sep 2020 20:13:54 GMT
USER ContainerUser
# Thu, 01 Oct 2020 22:19:53 GMT
ENV JAVA_VERSION=16-ea+18
# Thu, 01 Oct 2020 22:20:31 GMT
COPY dir:9823f48939163fc0e49dda85ad7963915dfd6567b20b9c5a7d861c5ae216b54a in C:\openjdk-16 
# Thu, 01 Oct 2020 22:20:58 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Thu, 01 Oct 2020 22:20:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecf9bb62dc6eedea9fd367628f8715dea75b7d2053afa4b5121e7809aa692139`  
		Size: 101.2 MB (101239122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f72ec155bceaba8b4a5cdbd7aa79586c7296a801af5364a691c46191c910e2da`  
		Last Modified: Tue, 08 Sep 2020 22:29:01 GMT  
		Size: 864.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b2192657885f813dd6fa78d8ba65d02e35934c0c45121f5cb3004298998876`  
		Last Modified: Tue, 08 Sep 2020 22:28:59 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe914594cd5b7b9a0b5c0080fe6c643b51eecedb3197955dbea30a0005a9132`  
		Last Modified: Tue, 08 Sep 2020 22:28:59 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4324dc65079aab4e95e3a823193385145a250bbb9e13cd9c5e02a35844069217`  
		Last Modified: Tue, 08 Sep 2020 22:29:00 GMT  
		Size: 65.1 KB (65142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bee2eb45cc55aae1760d1937d9de7b70abd95c9488b97a8288d08b472684fb5`  
		Last Modified: Tue, 08 Sep 2020 22:28:57 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d68e30210786d0925e020d049bf29f97503f73cc332df042df88200cf5f89a`  
		Last Modified: Thu, 01 Oct 2020 22:30:10 GMT  
		Size: 840.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a9dccb5cdf96070354326b1cd8355d89b615be976fde37360a621288bf82ab`  
		Last Modified: Thu, 01 Oct 2020 22:30:35 GMT  
		Size: 192.2 MB (192182706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99de8c5f811a1fcb9101ab541d4b7caba64fedb7aeca125f777cf45d3faaba5c`  
		Last Modified: Thu, 01 Oct 2020 22:30:14 GMT  
		Size: 3.5 MB (3524436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8d13fc711e8d7ede950c6dc939071aa33dd33073c9a46d439800443549004f`  
		Last Modified: Thu, 01 Oct 2020 22:30:10 GMT  
		Size: 837.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
