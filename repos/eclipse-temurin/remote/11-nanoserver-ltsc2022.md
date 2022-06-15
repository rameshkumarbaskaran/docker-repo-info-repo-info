## `eclipse-temurin:11-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:7922bf1285541a90dfc77015f09eba809446cb8c839426f2fe321d8c8f33a5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.768; amd64

### `eclipse-temurin:11-nanoserver-ltsc2022` - windows version 10.0.20348.768; amd64

```console
$ docker pull eclipse-temurin@sha256:32792dbd6f8822591fea731f909c68efa0d3fa17bcf0e73f5f76a2e67a47e930
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.3 MB (310340815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681b3d48fe361af52e01854d0375413b235956a8e121a6e958cd94756f8de60b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jun 2022 04:10:14 GMT
RUN Apply image 10.0.20348.768
# Wed, 15 Jun 2022 18:08:52 GMT
SHELL [cmd /s /c]
# Wed, 15 Jun 2022 18:10:34 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Wed, 15 Jun 2022 18:10:35 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 15 Jun 2022 18:10:36 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 18:10:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jun 2022 18:10:49 GMT
USER ContainerUser
# Wed, 15 Jun 2022 18:11:06 GMT
COPY dir:1583ce76f01a2d0a0742f7b70646c210ef8c619565a381c37e5a1156f6ec4636 in C:\openjdk-11 
# Wed, 15 Jun 2022 18:11:25 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 Jun 2022 18:11:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fca88290e1b048d74ec4e9d1548c4ec09dc3921f80285f39a186278fcaf2d86f`  
		Size: 118.0 MB (117976537 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:60cbdb7704dc53714205f32082d3faa20d7c93a53c40cb88f22581e85a2943fc`  
		Last Modified: Wed, 15 Jun 2022 19:13:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e15212970b6845299234e1cad297412ba0475a85606f84621dbc838887768b8`  
		Last Modified: Wed, 15 Jun 2022 19:16:39 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b0d966a898e55955065e11f87c837d08fedde78b24ae024f6ec9f079b4e9ba`  
		Last Modified: Wed, 15 Jun 2022 19:16:39 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2194672c015e9948e535c97a56cc789af8a4bf39fe31ae529665a1640ec52b`  
		Last Modified: Wed, 15 Jun 2022 19:16:39 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c958ff41922bf54976a2f92edbaf407a4231daed2478c4d5aa66883ed9ccb2cc`  
		Last Modified: Wed, 15 Jun 2022 19:16:36 GMT  
		Size: 75.7 KB (75660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638f574defd9dc8ff7f223723c4405df39ef818975a4b8e1c7fc1b52f03c6272`  
		Last Modified: Wed, 15 Jun 2022 19:16:36 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd1803304d6f1bb50ecb1b421dbd849a76883e6c2d04604be2634435e75ec613`  
		Last Modified: Wed, 15 Jun 2022 19:20:01 GMT  
		Size: 192.2 MB (192219555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d137d4b4b79cd614ca1a82968359e2df0a60bad5be6df212d4ad25a29c09085`  
		Last Modified: Wed, 15 Jun 2022 19:16:36 GMT  
		Size: 62.3 KB (62278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de28e396da78ea71fc2be17f2266b026b5a89f3468e2adfca1e4bd3eef9552b`  
		Last Modified: Wed, 15 Jun 2022 19:16:37 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
