## `eclipse-temurin:19-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:b60d43b53cc84df8663e4950f6d218cc30c9b9e95574822af129e1ce739a323d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:19-nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull eclipse-temurin@sha256:a989b7ce404d9bde106808af1fbb77501c1a943ef9ae7a9b104e38071a8047d9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300261658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e783f2028cc651f6729559015e0b90b91016222f4ff778efcd3e872aa1643046`
-	Default Command: `["jshell"]`
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
# Mon, 26 Sep 2022 23:22:52 GMT
COPY dir:f9e4978cc3e169a38f06094f4d9bd0ec177b4256ff40cd3387fc1d393235d05c in C:\openjdk-19 
# Mon, 26 Sep 2022 23:23:10 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 26 Sep 2022 23:23:11 GMT
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
	-	`sha256:f0744a0c8d0119903fe90096119d2d0cd5367760b5ce3b9e9c3ecdd1b165d7c6`  
		Last Modified: Mon, 26 Sep 2022 23:34:04 GMT  
		Size: 193.2 MB (193156778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7b4d594fd6189e65fcb0118ecfc972ea70f37ace8310daafa31a8352a2184f`  
		Last Modified: Mon, 26 Sep 2022 23:33:45 GMT  
		Size: 3.7 MB (3683369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3ddedb33c0e87c4470b9d16d4f89c41c4ec9f32ad2630d82f746a943af52d1`  
		Last Modified: Mon, 26 Sep 2022 23:33:44 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
