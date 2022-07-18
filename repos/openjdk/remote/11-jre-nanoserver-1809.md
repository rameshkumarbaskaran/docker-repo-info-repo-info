## `openjdk:11-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:b852734c7a8417ad5ccd95cb243ec4fc58c9c05d9286ca13457ef8efce0ad74e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `openjdk:11-jre-nanoserver-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull openjdk@sha256:a570ae8cffcc839fd47f0e1444f03a7c846a33b018e441aa18cb657f68877bd4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142788054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc00455313ea0decaa48a8e8698b3f14b272527e0f184b6308960bc66bf10f65`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:50:41 GMT
SHELL [cmd /s /c]
# Wed, 13 Jul 2022 16:06:40 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 13 Jul 2022 16:06:41 GMT
USER ContainerAdministrator
# Wed, 13 Jul 2022 16:06:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 Jul 2022 16:06:49 GMT
USER ContainerUser
# Wed, 13 Jul 2022 16:06:50 GMT
ENV JAVA_VERSION=11.0.15
# Wed, 13 Jul 2022 16:09:50 GMT
COPY dir:b19a7bc4e0a7772217140b5b5a40fc0497b9874821c6267cef822ccc10258697 in C:\openjdk-11 
# Wed, 13 Jul 2022 16:10:05 GMT
RUN echo Verifying install ... 	&& echo   java --version && java --version 	&& echo Complete.
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b09c07c6aeead64423fdefc240fe2e1b6330c96732fd2705113030da84416be`  
		Last Modified: Mon, 18 Jul 2022 21:22:33 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1234d8139b62fe1cc2af73e6f7e19087c38bbf27b1301126e4825445a53129ba`  
		Last Modified: Mon, 18 Jul 2022 21:29:22 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fb8775c7c189c574b2c2e9559d8e0069174344caf6a8e82a8a8311e9b46649`  
		Last Modified: Mon, 18 Jul 2022 21:29:22 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48e18300deee27181a3e362a7857b5e4f7d95ad751f96a0b3fff63f97d8ba0f`  
		Last Modified: Mon, 18 Jul 2022 21:29:22 GMT  
		Size: 69.0 KB (68975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31f1cf222f09294611ee30eb57920d0e6ee6e7aecd5a3d0d0ce758b70f63b33`  
		Last Modified: Mon, 18 Jul 2022 21:29:20 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8150b82482f26bc71fcdbb1b6298a2881ddcfca3968939f14bce19e137969245`  
		Last Modified: Mon, 18 Jul 2022 21:29:20 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7fb8e0a0bcb5961cab647ec4ded0f7b96f702b3ddc626b1a4ddaa6218e5324`  
		Last Modified: Mon, 18 Jul 2022 21:30:50 GMT  
		Size: 39.5 MB (39476748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ccf6aac11adeb901ece11beb69edd4bad815fc8362080b0c6b97247069fc46`  
		Last Modified: Mon, 18 Jul 2022 21:30:42 GMT  
		Size: 81.6 KB (81576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
