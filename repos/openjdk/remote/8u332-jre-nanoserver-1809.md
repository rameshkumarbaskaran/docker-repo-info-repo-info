## `openjdk:8u332-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:8de58f0bbdcd0e5a13bb2e88a9ab27d12744caa71caf59f5800b2e7869abfb1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `openjdk:8u332-jre-nanoserver-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull openjdk@sha256:1fb239c756b3f7a3bf2dda33b8fe0571fabeb79a27b370862f7af5b65da2dce2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141577782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4dc229048828aec057459f3391cc465daa05bf97b713b1f1d359956d111e00a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:50:41 GMT
SHELL [cmd /s /c]
# Wed, 13 Jul 2022 16:14:00 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Jul 2022 16:14:01 GMT
USER ContainerAdministrator
# Wed, 13 Jul 2022 16:14:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 Jul 2022 16:14:13 GMT
USER ContainerUser
# Wed, 13 Jul 2022 16:14:13 GMT
ENV JAVA_VERSION=8u332
# Wed, 13 Jul 2022 16:17:32 GMT
COPY dir:a69662fb25cadf36484d90c7c9990719015f86fa8a02dabf235af3b8f20f255b in C:\openjdk-8 
# Wed, 13 Jul 2022 16:17:46 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b09c07c6aeead64423fdefc240fe2e1b6330c96732fd2705113030da84416be`  
		Last Modified: Mon, 18 Jul 2022 21:22:33 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148f24fdace3fb9dfc469abd587650fafdf6306095591fbac5f681ea330560c0`  
		Last Modified: Mon, 18 Jul 2022 21:32:02 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f93316072971a85b9949521e5e6ecf59d21bdc3581fc1e1add713febb868ef0`  
		Last Modified: Mon, 18 Jul 2022 21:32:02 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed149726e806a0166236d15cf4fc5ea65eb1da4033351d46fa58aa3f704aa85`  
		Last Modified: Mon, 18 Jul 2022 21:31:59 GMT  
		Size: 72.7 KB (72654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fcf0621e58eee5b24877bc6f1542450faf983b06d868581b56b39dc69597f3`  
		Last Modified: Mon, 18 Jul 2022 21:31:59 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c95bf4d1ff3d66693e0ce009d29f62edeb2992004e2227a8611a034f690155`  
		Last Modified: Mon, 18 Jul 2022 21:31:59 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49ab983371d930f66e7d746bafdd9c927219d4a67a9a183a01baf8d2003f6bc`  
		Last Modified: Mon, 18 Jul 2022 21:33:08 GMT  
		Size: 38.3 MB (38288883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17341066350484641b752dc726f6640d72c46d56fbbdd774f036e11bb2cfddf`  
		Last Modified: Mon, 18 Jul 2022 21:33:02 GMT  
		Size: 55.5 KB (55499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
