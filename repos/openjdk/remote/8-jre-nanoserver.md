## `openjdk:8-jre-nanoserver`

```console
$ docker pull openjdk@sha256:97c43153bb7d9bcea425a7ae76510330e73368e9187a541b3b2eabd267884270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `openjdk:8-jre-nanoserver` - windows version 10.0.17763.1098; amd64

```console
$ docker pull openjdk@sha256:eb18fcff5e9b95ccee2a7da5827e04acabf10f0be7ddac441d880456f15d314d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.6 MB (200645723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34c1ffbc8e59515928f01156c7c67c059dd42cad42792dea18416c57461b76f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:56:25 GMT
SHELL [cmd /s /c]
# Wed, 11 Mar 2020 15:17:50 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 11 Mar 2020 15:17:52 GMT
USER ContainerAdministrator
# Wed, 11 Mar 2020 15:18:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 11 Mar 2020 15:18:10 GMT
USER ContainerUser
# Wed, 11 Mar 2020 15:18:11 GMT
ENV JAVA_VERSION=8u242
# Wed, 11 Mar 2020 15:19:01 GMT
COPY dir:604850e4892a2e6375b4d95fb378e9776042497a20a33de1bbe6b0d17fade1d2 in C:\openjdk-8 
# Wed, 11 Mar 2020 15:21:00 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4a66be005a5120fc8bbc31290c77aa0e6580d02bc61948ef0602bf09a6ab61ba`  
		Last Modified: Wed, 11 Mar 2020 15:26:11 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e12110bee2e2272415f9ff8bc488e8e4a02d2919d8f9f817bdf68365de6865`  
		Last Modified: Wed, 11 Mar 2020 15:36:56 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba96096a7ae0c48bc767128f42b13d0fab67eef3e7fb789b30f93a66a4745b01`  
		Last Modified: Wed, 11 Mar 2020 15:36:55 GMT  
		Size: 927.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09890c106af2276d23a2b55aa6f671da3c3561c10338e16f426d0edbe6859c12`  
		Last Modified: Wed, 11 Mar 2020 15:36:52 GMT  
		Size: 68.8 KB (68837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd471ddcc22d30335908979571e259e9f1591bb72eb3a43699b37edd063b12df`  
		Last Modified: Wed, 11 Mar 2020 15:36:53 GMT  
		Size: 906.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc3ac250e8be70b9662709f5f2287f67150dad5c7758c060920c4613b2ffa39`  
		Last Modified: Wed, 11 Mar 2020 15:36:52 GMT  
		Size: 936.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e52dceebf7d88238a4f27794a3f093288e2452ea5d0ab4ddcb105c971613a3`  
		Last Modified: Wed, 11 Mar 2020 15:37:10 GMT  
		Size: 99.5 MB (99476408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b4e2e559451dbf5dbeac869cfde1cdc3bd7675838326ef147dde3adda0231d`  
		Last Modified: Wed, 11 Mar 2020 15:37:47 GMT  
		Size: 45.6 KB (45598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
