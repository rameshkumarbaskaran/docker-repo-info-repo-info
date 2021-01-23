## `openjdk:16-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:4933bde138fc07686d19d0d743146e9b5c88b893615b763972279262a75aaa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:16-jdk-nanoserver` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:d7307b2540e1cc7ffed102b36193c23abff4571f31743334ed8170d3f7f6086a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285141767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c886610fd69e50c56f562d465a71934f2bd0d8bccda502bfbf97d8c1a92e8feb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:56:48 GMT
SHELL [cmd /s /c]
# Wed, 13 Jan 2021 20:35:00 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 13 Jan 2021 20:35:01 GMT
USER ContainerAdministrator
# Wed, 13 Jan 2021 20:35:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 13 Jan 2021 20:35:14 GMT
USER ContainerUser
# Sat, 23 Jan 2021 01:25:38 GMT
ENV JAVA_VERSION=16-ea+33
# Sat, 23 Jan 2021 01:26:10 GMT
COPY dir:e3ddb60c7382bc57009cc229bac1129c57da026b489d0e41e419c48589e07431 in C:\openjdk-16 
# Sat, 23 Jan 2021 01:26:30 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Sat, 23 Jan 2021 01:26:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c2b6c001c337f812bceb3b03d15a70d1d9905540658e751e42f20f7cc0ddc819`  
		Last Modified: Wed, 13 Jan 2021 21:16:47 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22f53d1f631e14bb9677766dc089ce4caf4dae9627d1513773cfff289e94f42`  
		Last Modified: Wed, 13 Jan 2021 21:19:22 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43af010a68e2978961a3d63887efbc1230811009f66bd683e9fc4174f4185177`  
		Last Modified: Wed, 13 Jan 2021 21:19:20 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3132f9cb979d43ab9de9d926bc492cf9bd38763c7e557f278fe358ac557f14b6`  
		Last Modified: Wed, 13 Jan 2021 21:19:19 GMT  
		Size: 65.1 KB (65097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d6c42dd2fabc75c92d7f5ad83fa610805a5e5dea3aba8da7ef9c4271f5ec93`  
		Last Modified: Wed, 13 Jan 2021 21:19:16 GMT  
		Size: 937.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f83716f517b5bf903380377e3fcd73b0e7cc0c251f52f5d90cf9431e340021`  
		Last Modified: Sat, 23 Jan 2021 01:45:14 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2480c1d7d207f1e55022f8d8ece7289696517e2ce05958af2b53e119d2c4ae3`  
		Last Modified: Sat, 23 Jan 2021 01:48:33 GMT  
		Size: 180.0 MB (180032861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebfc0b8723b73f5ce7ecc6a905a60a1a13555699077abb4046d2d0b65e8dab8`  
		Last Modified: Sat, 23 Jan 2021 01:45:18 GMT  
		Size: 3.7 MB (3697786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6b717b70d7b50d098011408cf9138c7f9771156d6a026fedeeb34fe1c763cb`  
		Last Modified: Sat, 23 Jan 2021 01:45:14 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
