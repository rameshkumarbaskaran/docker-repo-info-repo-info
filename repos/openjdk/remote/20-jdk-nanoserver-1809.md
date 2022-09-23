## `openjdk:20-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:302e33c56f985b1643a60c5377c3183478d36e48b1e7863faf0bb2d4f5151112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `openjdk:20-jdk-nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull openjdk@sha256:b10a1ce2671f821c103bab30b2758efb0db21c06d0f3260063b3929693b5d965
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.0 MB (299003296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34673ead8f5de2058c725359357f8a916147c000db81e00b1c424f424cb63801`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 16:03:00 GMT
SHELL [cmd /s /c]
# Wed, 14 Sep 2022 17:08:57 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 14 Sep 2022 17:08:57 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 17:09:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Sep 2022 17:09:07 GMT
USER ContainerUser
# Fri, 23 Sep 2022 00:36:41 GMT
ENV JAVA_VERSION=20-ea+16
# Fri, 23 Sep 2022 00:36:56 GMT
COPY dir:6f80cca3988e744affd0c6bdf0a6237277922586584d294879f1340cb5579f67 in C:\openjdk-20 
# Fri, 23 Sep 2022 00:37:14 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 23 Sep 2022 00:37:15 GMT
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
	-	`sha256:6f67cb607010c6768708866762c8f245af049da7669af90242ea7dc3d1881f80`  
		Last Modified: Wed, 14 Sep 2022 17:22:54 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbd0c7e3fefcb9d81347f1ab494f4177ae8fff7d71ac827f5e90d34ee4bf483`  
		Last Modified: Wed, 14 Sep 2022 17:22:54 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72046412150cabb4b6b5ba4cf56188800073ddce5f570b7d921bc62eb13c577`  
		Last Modified: Wed, 14 Sep 2022 17:22:54 GMT  
		Size: 67.8 KB (67836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea99aee812db540f38ee961b7634ec0afe7d8468d85e3adaabe234fee1414d5`  
		Last Modified: Wed, 14 Sep 2022 17:22:51 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819d67ce8ff461f082dcb2fccfb9aac5fceb67dcd69f871b5da9de2b22d81b84`  
		Last Modified: Fri, 23 Sep 2022 00:40:20 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b757ad2addbc3f496e66637c3dcaf5c02d9a12b200061b13a125c9fdc6bf0b`  
		Last Modified: Fri, 23 Sep 2022 00:40:39 GMT  
		Size: 191.8 MB (191842161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e92d4296fd1009d053f75ff46ca372a75e700966f82c9cb326c7a2de333915`  
		Last Modified: Fri, 23 Sep 2022 00:40:21 GMT  
		Size: 3.8 MB (3752155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91eccda7c786dec2bb2dfeda8619589fa2fdccb6eac00ffe1c48afd0111be39e`  
		Last Modified: Fri, 23 Sep 2022 00:40:20 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
