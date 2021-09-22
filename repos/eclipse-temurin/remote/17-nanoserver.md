## `eclipse-temurin:17-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:c36665ae585d09ae395f19daeba2ad50f1031eb6d7ef16d1cfc71063f883b763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `eclipse-temurin:17-nanoserver` - windows version 10.0.17763.2183; amd64

```console
$ docker pull eclipse-temurin@sha256:c96aba78cca3ccc0ff8dc7f40113c6a5e7caf37e4f661a485e0585161de85cf6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.4 MB (291368263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8676ae9b160b45f71f1488d927a1a589adbaca787fe34e6f53963e96d821dea`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 00:38:23 GMT
SHELL [cmd /s /c]
# Wed, 22 Sep 2021 19:22:12 GMT
ENV JAVA_VERSION=jdk-17+35
# Wed, 22 Sep 2021 19:22:13 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 22 Sep 2021 19:22:14 GMT
USER ContainerAdministrator
# Wed, 22 Sep 2021 19:22:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 22 Sep 2021 19:22:28 GMT
USER ContainerUser
# Wed, 22 Sep 2021 19:22:47 GMT
COPY dir:ba92fda3ecc57988e3fdb5e98847d06c9e695148297ce16b53bb487a02cbd557 in C:\openjdk-17 
# Wed, 22 Sep 2021 19:23:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 22 Sep 2021 19:23:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:807d06303c39b2317729754a4c7ad6501e59c16ee464f8f671f9947774f62f72`  
		Last Modified: Wed, 15 Sep 2021 01:10:56 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ab8e009ab1dd301c82841e08b88f07605e79634d732f5c7c8ab22448543df8`  
		Last Modified: Wed, 22 Sep 2021 19:26:27 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4ca02cde604d042d5b52a4bcf0903ceef3e5425869c960eda909a4799f0525`  
		Last Modified: Wed, 22 Sep 2021 19:26:27 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b902f71b18595f7c38de37caeb7758215687f9faa4c4c38f465562a69721b708`  
		Last Modified: Wed, 22 Sep 2021 19:26:27 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4b382a2dfe77e8a93fdd258a3edcafb0a0661d3b2c2db0928628b190d4af35`  
		Last Modified: Wed, 22 Sep 2021 19:26:24 GMT  
		Size: 70.1 KB (70063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f3e88ebe86ac33c5f6a58bb67887729fd314a54b83241ca075b33da233cced`  
		Last Modified: Wed, 22 Sep 2021 19:26:24 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04e00e59d5a0dd9fe289f6e95f0fcb05f4be37123ea770bda5fd09f27a7078d`  
		Last Modified: Wed, 22 Sep 2021 19:26:45 GMT  
		Size: 184.9 MB (184938496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88708eb5a5e394f74e0cdfebc4987e33d9572536e98f15446b12bd4f61bc6135`  
		Last Modified: Wed, 22 Sep 2021 19:26:25 GMT  
		Size: 3.6 MB (3649667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a6dadbc9f0efe3aaf3a0dcdaa9598857e639ab60f334724f305bd34c7d1948`  
		Last Modified: Wed, 22 Sep 2021 19:26:24 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
