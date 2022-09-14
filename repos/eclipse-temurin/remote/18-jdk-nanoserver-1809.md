## `eclipse-temurin:18-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:4a3c97b737bf85ecf137ce29cb6b3885be84cdd70892e341f23241c3d0175684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:18-jdk-nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull eclipse-temurin@sha256:f5fda0b623d87e19e261fd851b4439388532f30443b5c07876ef3785743e1ab4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293520919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492dc1f619c907244630c3789dd0f79a4a4230822d682ecbddb731d12d5a5b9f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 16:03:00 GMT
SHELL [cmd /s /c]
# Wed, 14 Sep 2022 16:32:58 GMT
ENV JAVA_VERSION=jdk-18.0.2.1+1
# Wed, 14 Sep 2022 16:32:59 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 14 Sep 2022 16:33:00 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 16:33:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Sep 2022 16:33:09 GMT
USER ContainerUser
# Wed, 14 Sep 2022 16:33:23 GMT
COPY dir:ae9d728ada666b27b908f8727aedf35273804bd829b96771abae3f99230f2142 in C:\openjdk-18 
# Wed, 14 Sep 2022 16:33:38 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 14 Sep 2022 16:33:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:233f09b2a52487084f2cfb5e06dac2815651432c9d37c729582f59cfcf66b243`  
		Last Modified: Wed, 14 Sep 2022 16:47:12 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a350d08f2ed032e24a5320519566197931177aa31b5e885df487768aa2d5f5`  
		Last Modified: Wed, 14 Sep 2022 16:55:55 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c756bccc16e99f889fd3cddef91c4c843400008c3236a93d522dd8bc69cce823`  
		Last Modified: Wed, 14 Sep 2022 16:55:55 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042bd3a9ce1e44b5ff9dcfe43afee3fad7b479a685801f33f3a34f6da4f5a995`  
		Last Modified: Wed, 14 Sep 2022 16:55:54 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3b136eeda7e8702846403916f3e784b1e6c907e6bc2f75959527c202b647ef`  
		Last Modified: Wed, 14 Sep 2022 16:55:52 GMT  
		Size: 68.4 KB (68403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03d8d62f82ad88c842779be7d22f04938ffd988a725584682799412da4f8d3b`  
		Last Modified: Wed, 14 Sep 2022 16:55:52 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00915b2ff303ff81b8393f258a74c1b15496495b82c184f100656482ce230ee`  
		Last Modified: Wed, 14 Sep 2022 16:56:13 GMT  
		Size: 186.6 MB (186551047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438c464bcb6794ae81cc9c3f5bbdcd87c9ef798628d286dc1a1b2862a6187050`  
		Last Modified: Wed, 14 Sep 2022 16:55:52 GMT  
		Size: 3.6 MB (3560383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191799a501f6b59a485f2d035c6bf68b0e6ac0a2724c44a5d1718899e7cbbd60`  
		Last Modified: Wed, 14 Sep 2022 16:55:52 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
