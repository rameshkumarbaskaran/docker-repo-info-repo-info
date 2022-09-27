## `eclipse-temurin:19_36-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:be0632f5f5ab79d0e808c62e372c35b73d7193377b1a1e4798a5111fbb4c2ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:19_36-jre-nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull eclipse-temurin@sha256:30262f1c5c625f83d5fc3663174ac8c306b9f260649d09709cb0f4b96ab64624
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151582514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ade68bd409605214d13fd1bc22a8b35de87c140eb59b7d1bf8491585705dac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 16:03:00 GMT
SHELL [cmd /s /c]
# Mon, 26 Sep 2022 23:22:21 GMT
ENV JAVA_VERSION=jdk-19+36
# Mon, 26 Sep 2022 23:22:22 GMT
ENV JAVA_HOME=C:\openjdk-19
# Mon, 26 Sep 2022 23:22:22 GMT
USER ContainerAdministrator
# Mon, 26 Sep 2022 23:22:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Mon, 26 Sep 2022 23:22:36 GMT
USER ContainerUser
# Mon, 26 Sep 2022 23:27:26 GMT
COPY dir:941cb8f5f97f3f5d2a48807df827e977e3ea22f3a1de758e43d87dd2ec67a41d in C:\openjdk-19 
# Mon, 26 Sep 2022 23:27:40 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:233f09b2a52487084f2cfb5e06dac2815651432c9d37c729582f59cfcf66b243`  
		Last Modified: Wed, 14 Sep 2022 16:47:12 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64127987a70d808bacf6dcbbc07a4a1a4a083fa6d4000191f8386f2aabe0cfa`  
		Last Modified: Mon, 26 Sep 2022 23:33:46 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba1d952cacc3305ba2f5bc748e79106a58c170a3b0528b1d408358b8806bfa`  
		Last Modified: Mon, 26 Sep 2022 23:33:46 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43527b3b075cc7216324bd1221cbe139b9bc294fab2f3a09e6834e445fcd50e0`  
		Last Modified: Mon, 26 Sep 2022 23:33:47 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdf5099fa33d2e7d72b252a73ffa36451e0816b72352792d48c9abd16aeb5ad`  
		Last Modified: Mon, 26 Sep 2022 23:33:44 GMT  
		Size: 80.3 KB (80335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb34c9b6aba6b7a775e239d7a3e86675ab3758215b1685ae5ad3c4eda4dd24ad`  
		Last Modified: Mon, 26 Sep 2022 23:33:44 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a33716f2d788574aaca5babce032a090fcfba03e63160646e4fb440c5a1b2`  
		Last Modified: Mon, 26 Sep 2022 23:35:06 GMT  
		Size: 45.1 MB (45103261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee49bc3ae2446ddd846b82fe08ec0de6406ba1105c6bff99899b7af56581375c`  
		Last Modified: Mon, 26 Sep 2022 23:34:58 GMT  
		Size: 3.1 MB (3058915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
