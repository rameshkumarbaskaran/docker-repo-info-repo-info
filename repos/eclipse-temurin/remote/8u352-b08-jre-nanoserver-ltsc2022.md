## `eclipse-temurin:8u352-b08-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:82eac03a5d3b1de3fcc24f7dcc1c8bb1f802e0d0d29af67afa1714cb452bc454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `eclipse-temurin:8u352-b08-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1129; amd64

```console
$ docker pull eclipse-temurin@sha256:31ddfae865d2159baf99c76e2407ace1c1f68522b12c758de8092e5f44f65761
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161480895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e3c50402d68cdba3b4898a7cfd44ce13451308606e858c8eafea619f3f9757`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Oct 2022 21:37:41 GMT
RUN Apply image 10.0.20348.1129
# Wed, 12 Oct 2022 15:54:21 GMT
SHELL [cmd /s /c]
# Fri, 04 Nov 2022 23:39:15 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:39:16 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 04 Nov 2022 23:39:17 GMT
USER ContainerAdministrator
# Fri, 04 Nov 2022 23:39:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 04 Nov 2022 23:39:38 GMT
USER ContainerUser
# Fri, 04 Nov 2022 23:40:33 GMT
COPY dir:4e862dd3e9e3173048336ba652726d009cc7bbbadd67bc711cdb421cf611c5ab in C:\openjdk-8 
# Fri, 04 Nov 2022 23:40:50 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:b6520318982addabaf67d0cef5499282d15348f205cf5d7328925bcd681e85bd`  
		Last Modified: Tue, 25 Oct 2022 22:04:15 GMT  
		Size: 122.0 MB (122003513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ed0041e3584df1952980c3f73fd2b6e154328c7a0165f37dbe92ef94ae8a95`  
		Last Modified: Wed, 12 Oct 2022 16:12:53 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95809cf8ef923c767b7953d30af5ca933179ebe310f41272c94409628ab7317`  
		Last Modified: Sat, 05 Nov 2022 00:26:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb651dc877e82864217b0cc3ce7819ed73fe3099aae266fde4d8371b8fc61766`  
		Last Modified: Sat, 05 Nov 2022 00:26:51 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d82c60c747cd53aa1eba03c2c4a811bea3ce486fa34e6fff7133b6db31383d`  
		Last Modified: Sat, 05 Nov 2022 00:26:49 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9db15f529310d0afff94586feed5c2e8342060c276755e3f12324acd35f5b7b`  
		Last Modified: Sat, 05 Nov 2022 00:26:49 GMT  
		Size: 85.2 KB (85211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d3c46d9d9cd54570a0d0df563ff06fc76ffb006db566305ff75b5099c3b4fd`  
		Last Modified: Sat, 05 Nov 2022 00:26:49 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011e8c45d98254bc274f7acb7c149f61c829bbb62d918888d9515ad67c8d8323`  
		Last Modified: Sat, 05 Nov 2022 00:27:22 GMT  
		Size: 39.3 MB (39324559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223ed96b94cafd273f19b5cc72eb3ef771fb27a1dcf1ad5b3c650090dbcd7fb4`  
		Last Modified: Sat, 05 Nov 2022 00:27:16 GMT  
		Size: 61.9 KB (61900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
