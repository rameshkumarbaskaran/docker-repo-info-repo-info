## `eclipse-temurin:19-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:558503cfc0da8437fd417541cc2e783369fb989df52891b2be0fc53e8cd96a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:19-nanoserver` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:8a029c79fa84b6b139fa5c0c3c0a73f09a4b05cfab9a45427afd98c1b775e448
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.4 MB (311444076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683ce923efb13e186352c7a8b13b23c4832936bcf1eca6982d26e24a7439ea1c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Sep 2022 20:11:22 GMT
RUN Apply image 10.0.20348.1006
# Wed, 14 Sep 2022 16:38:20 GMT
SHELL [cmd /s /c]
# Mon, 26 Sep 2022 23:28:21 GMT
ENV JAVA_VERSION=jdk-19+36
# Mon, 26 Sep 2022 23:28:22 GMT
ENV JAVA_HOME=C:\openjdk-19
# Mon, 26 Sep 2022 23:28:23 GMT
USER ContainerAdministrator
# Mon, 26 Sep 2022 23:28:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Mon, 26 Sep 2022 23:28:38 GMT
USER ContainerUser
# Mon, 26 Sep 2022 23:28:54 GMT
COPY dir:f9e4978cc3e169a38f06094f4d9bd0ec177b4256ff40cd3387fc1d393235d05c in C:\openjdk-19 
# Mon, 26 Sep 2022 23:29:16 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 26 Sep 2022 23:29:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:09629875cd6ee57fa551626fa2963d8b54718ba9acbf28e7cb5d684a9cb754d7`  
		Size: 118.1 MB (118131331 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:07f30e2ceaa03f6ac7b6e6f319083288f48d1fa2a61f36f51f516da241496976`  
		Last Modified: Wed, 14 Sep 2022 16:57:28 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864919bef3913744b28c53273341a0b0ec4a3c1785d5140ac9f4e3e94e1a5578`  
		Last Modified: Mon, 26 Sep 2022 23:35:22 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc56ee6307a1b64af8969055dbc830e5ff5920fa53ebd6eb48accb9ab328499`  
		Last Modified: Mon, 26 Sep 2022 23:35:22 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402c82e82d21c41f5c1a221c457c0fde325671f19b742915fd2772c5fb8ab083`  
		Last Modified: Mon, 26 Sep 2022 23:35:22 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef34e0a52f3fadf98a0ccef1daf4579718ab2d54cdd9cdf7613fe123578a90bb`  
		Last Modified: Mon, 26 Sep 2022 23:35:20 GMT  
		Size: 80.5 KB (80480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9149f802f4ccb5a15b71877a120f3968cfefd4bc9d29f9732a691572ccbc2c`  
		Last Modified: Mon, 26 Sep 2022 23:35:20 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8ffe94dd1ceabd0eb71d354637c43b6e02d4bce509efd8708fd1361ff0d6ba`  
		Last Modified: Mon, 26 Sep 2022 23:35:40 GMT  
		Size: 193.2 MB (193162297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdb73422e29c8fa192f29874017bb6f8b64f3f315f8f377313874208f8c8fbf`  
		Last Modified: Mon, 26 Sep 2022 23:35:20 GMT  
		Size: 63.1 KB (63122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48fa9c790564d1282c5246c19c0f24284a094ab082aa941fa1fb3b4cd3281ca`  
		Last Modified: Mon, 26 Sep 2022 23:35:20 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-nanoserver` - windows version 10.0.17763.3406; amd64

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
