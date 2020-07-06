## `openjdk:15-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:7d1c1f17b6fc2ce21d1aa61af621dff1c6f22b0b09aab0aff7917ae028fb67b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `openjdk:15-jdk-nanoserver-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull openjdk@sha256:a38f29c6a914e501cd3f02a09d667cd9ab6b4be828f89e31b8cb8d449a158254
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295944360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e9a9d0c94e7f029692d215e4cb15252025723e43b79c7db048b8d5f9adeabc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jun 2020 11:12:32 GMT
RUN Apply image 1809-amd64
# Tue, 09 Jun 2020 22:42:44 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2020 22:42:45 GMT
ENV JAVA_HOME=C:\openjdk-15
# Tue, 09 Jun 2020 22:42:45 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2020 22:43:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Tue, 09 Jun 2020 22:43:01 GMT
USER ContainerUser
# Mon, 06 Jul 2020 20:58:16 GMT
ENV JAVA_VERSION=15-ea+30
# Mon, 06 Jul 2020 20:59:09 GMT
COPY dir:3e91297b5817dc6d7e8a18fb7fe08dd560f3d2ba3fb90ac833ff85de50911a31 in C:\openjdk-15 
# Mon, 06 Jul 2020 20:59:26 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Mon, 06 Jul 2020 20:59:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c7d6d47ff7dfb2aa4d4e819641b93ec971e8541978dff0ffc24c193babeb8c07`  
		Size: 101.0 MB (101043386 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5b390ee94e41353252b153770fa99d748992b90bdaf9abf7c785d93be52ee02c`  
		Last Modified: Tue, 09 Jun 2020 23:19:14 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a124a49383ae5eb05208979bcfbadf68055d2672da7f78201fe9a45e8d0bbb`  
		Last Modified: Tue, 09 Jun 2020 23:19:14 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb0c11b8fc0c6457077b02c8314626c0346af177c44a8615448f933e94b909c`  
		Last Modified: Tue, 09 Jun 2020 23:19:13 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29f17e75290909d8f60805f97895317f25ce6c2dc53b1b25e8d6dfe142e6f53`  
		Last Modified: Tue, 09 Jun 2020 23:19:13 GMT  
		Size: 63.5 KB (63500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fe65db6982f49c866229851adc1c64f6e6354b9e0a49d506241693ac2e660f`  
		Last Modified: Tue, 09 Jun 2020 23:19:11 GMT  
		Size: 814.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2c888f067ef85b28ae8c22baf48c8ebc8407efdcbd9e1e3659c68d7b830e63`  
		Last Modified: Mon, 06 Jul 2020 21:07:26 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050b479f16eef3d6f7fc7f0dfe2be53caa801a6aae903daff7709b6134765f24`  
		Last Modified: Mon, 06 Jul 2020 21:07:48 GMT  
		Size: 191.3 MB (191318574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459d8f9128b1e55ec04546eeee3d1c04e5c7224d9f4dbcc4435b292d4467d124`  
		Last Modified: Mon, 06 Jul 2020 21:07:28 GMT  
		Size: 3.5 MB (3513804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44561f39e2aaafc3d413363f5916ce1a28f6a500a4e5598c576418bb7819cff8`  
		Last Modified: Mon, 06 Jul 2020 21:07:26 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
