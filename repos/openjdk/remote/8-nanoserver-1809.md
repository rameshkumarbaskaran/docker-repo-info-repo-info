## `openjdk:8-nanoserver-1809`

```console
$ docker pull openjdk@sha256:999a8f16d355690d9e9931d5a5af908874d68a12d3aa87bbb5133c20ae9cfaa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `openjdk:8-nanoserver-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull openjdk@sha256:624e51cd6200f7067a33a0adbf36f0c2cd7453bda0254bf2072799eeccff08ef
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200654163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fa43c76fff8679d2107cf3732e6254ef83e6b6d3bc660ddcffde3d3d6563c2`
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
# Wed, 11 Mar 2020 15:19:20 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version
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
	-	`sha256:9af80821ad0c6592a77f194888947587bed4a605e6ff8ccbd56f78662d5af464`  
		Last Modified: Wed, 11 Mar 2020 15:36:52 GMT  
		Size: 54.0 KB (54038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
