## `eclipse-temurin:17-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:9eb02b66215208556919731d02d1f609118ae4ba3ab9675df9593f2a2b0d80f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `eclipse-temurin:17-jre-nanoserver-1809` - windows version 10.0.17763.4252; amd64

```console
$ docker pull eclipse-temurin@sha256:523688b307373090c65f6c8a9697937d2dc7c39c02a2a25c508a055523fdada4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153196972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cba58fb9e42640133981f05eeb75680d9694a119dce8c5f130238a17973ee5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Tue, 11 Apr 2023 23:45:41 GMT
SHELL [cmd /s /c]
# Wed, 12 Apr 2023 01:25:11 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Wed, 12 Apr 2023 01:25:12 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Apr 2023 01:25:13 GMT
USER ContainerAdministrator
# Wed, 12 Apr 2023 01:25:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Apr 2023 01:25:24 GMT
USER ContainerUser
# Wed, 12 Apr 2023 01:30:34 GMT
COPY dir:bfcbd3aaadac52e2fbf5597edb59a69874950e88ce16232f7581c0ac600a935c in C:\openjdk-17 
# Wed, 12 Apr 2023 01:30:50 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:af799fb2ff133c89311c6a42d34b8cb6c9b11d775f52e04ab08389d05e64ed1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:10 GMT  
		Size: 106.8 MB (106788951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1db438f20b81fe0c031e4e3eee58d278fba7258d01057ff18964cccf70d41c`  
		Last Modified: Wed, 12 Apr 2023 00:52:38 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d940edd2c169dbe97e28eaac688f773a26971f49cbce0c580dec219c0a091a6`  
		Last Modified: Wed, 12 Apr 2023 09:40:59 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68cf891bc434751fa3e0d43803d1d1b3966b15191058fd5bf2d9f3f70340008`  
		Last Modified: Wed, 12 Apr 2023 09:40:59 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1662ed07c1d02bbfbbd979a470af707c2e65c7d8de779c6e791ca43a34f7ec`  
		Last Modified: Wed, 12 Apr 2023 09:40:59 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2804a413fa32f1ac8096607d75ad6a983b2755f9d7994a3275faa45ad68b44`  
		Last Modified: Wed, 12 Apr 2023 09:40:57 GMT  
		Size: 71.3 KB (71299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddad53a51d13c426f8e7d899d76b648e9ca0201514f6c69c5335ffc180da6eb0`  
		Last Modified: Wed, 12 Apr 2023 09:40:56 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a37308f9861194bc8b851e22bf983c1eeaaaac78de5dc81a7b61e1cdb1bf6aa`  
		Last Modified: Wed, 12 Apr 2023 09:42:19 GMT  
		Size: 43.3 MB (43294400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0143e56156090bc6418a948e585c4c215250811ced041e9ddd7cd246cd63d8d`  
		Last Modified: Wed, 12 Apr 2023 09:42:11 GMT  
		Size: 3.0 MB (3036561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
