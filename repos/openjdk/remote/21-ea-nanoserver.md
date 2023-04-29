## `openjdk:21-ea-nanoserver`

```console
$ docker pull openjdk@sha256:08f81331c167612c8b890a45bff7dae3997e804fdd0c81bcdd0c706ebe05fd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `openjdk:21-ea-nanoserver` - windows version 10.0.17763.4252; amd64

```console
$ docker pull openjdk@sha256:6cd80b66f9a87771380d1b32aebf9a56040f10458daac212b39788eec511d14d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307032382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ef168a7837ed37fef9bf54703b87ef6281bdd6660fbf55c0a06da6cd6d47a5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Tue, 11 Apr 2023 23:45:41 GMT
SHELL [cmd /s /c]
# Tue, 11 Apr 2023 23:45:42 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 11 Apr 2023 23:45:43 GMT
USER ContainerAdministrator
# Tue, 11 Apr 2023 23:45:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 11 Apr 2023 23:45:57 GMT
USER ContainerUser
# Fri, 28 Apr 2023 23:24:51 GMT
ENV JAVA_VERSION=21-ea+20
# Fri, 28 Apr 2023 23:25:06 GMT
COPY dir:14376cd05906f94f6779f75fced90941abcb9d012b371087a20a53a7add3c9d9 in C:\openjdk-21 
# Fri, 28 Apr 2023 23:25:17 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 28 Apr 2023 23:25:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af799fb2ff133c89311c6a42d34b8cb6c9b11d775f52e04ab08389d05e64ed1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:10 GMT  
		Size: 106.8 MB (106788951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1db438f20b81fe0c031e4e3eee58d278fba7258d01057ff18964cccf70d41c`  
		Last Modified: Wed, 12 Apr 2023 00:52:38 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959014ae4c354475658573dc2e10e98575d191deef98e1f23bf7cb9f4768408f`  
		Last Modified: Wed, 12 Apr 2023 00:52:37 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b662327c70093bac13b7d07354fdbcd6967cbc13aaac870ca2e077fafefceb8`  
		Last Modified: Wed, 12 Apr 2023 00:52:37 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9446ad09d009884e8a1db2085ef50cd6467dc3270eca7bac27fca70698013943`  
		Last Modified: Wed, 12 Apr 2023 00:52:37 GMT  
		Size: 68.0 KB (68014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1335b1a9f9197626e9424d9d24737142c9d98659cc7f5510ca10378488d00b51`  
		Last Modified: Wed, 12 Apr 2023 00:52:35 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b478f1d89724f170957bdc1eef3cca2ea5ce06153d9eaffc74fcdf0ee1bdecd7`  
		Last Modified: Fri, 28 Apr 2023 23:27:10 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f9e13c659facd2c571ec2e2bae3093afa1931dffd6b8ab2cc6c86986ed2aac`  
		Last Modified: Fri, 28 Apr 2023 23:27:29 GMT  
		Size: 196.4 MB (196373838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1bc1855e31c5be2a3178d84a6e45601dbe75c84328dd13a6a6805f32fb9e8e`  
		Last Modified: Fri, 28 Apr 2023 23:27:11 GMT  
		Size: 3.8 MB (3794872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41dd424e8e5dc9f71502f3e59dace8b4cf892cb12633905c77df67b2d6e4e0f`  
		Last Modified: Fri, 28 Apr 2023 23:27:10 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
