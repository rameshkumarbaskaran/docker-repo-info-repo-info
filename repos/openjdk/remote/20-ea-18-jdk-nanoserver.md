## `openjdk:20-ea-18-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:fb9b2192cc8e9271c35833fd82698f18fd1c087a2adc06f9c480f85667e17dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `openjdk:20-ea-18-jdk-nanoserver` - windows version 10.0.17763.3406; amd64

```console
$ docker pull openjdk@sha256:1accbeb05c40b449596ee5777da30bc2f0e6a908415686c2e8721ac72efc3d84
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.1 MB (299084572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d928d6e3397e8986eb68b1cac7c7df58d97129362fa80072c949c71b0c812aee`
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
# Fri, 07 Oct 2022 23:18:35 GMT
ENV JAVA_VERSION=20-ea+18
# Fri, 07 Oct 2022 23:18:49 GMT
COPY dir:483e8c5e7a9f569d5f056ca40e9cc5008b7d0f5f9a8d61a265181e1e2313d355 in C:\openjdk-20 
# Fri, 07 Oct 2022 23:19:15 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 07 Oct 2022 23:19:16 GMT
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
	-	`sha256:55e3ed4c3f634dd830419f7f6971dc638046ee14b325d1de65d7864fa5bd6954`  
		Last Modified: Fri, 07 Oct 2022 23:22:40 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b651070b36e1702c31cb0e98d93cf2a6afc9bab2985c448278e78d2107ffc66c`  
		Last Modified: Fri, 07 Oct 2022 23:23:01 GMT  
		Size: 191.9 MB (191923093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eef32d5eaaf43bd8b8919514232b201ea15918486c29cf5d072328785d6bcbf`  
		Last Modified: Fri, 07 Oct 2022 23:22:41 GMT  
		Size: 3.8 MB (3752480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c0c232e31fd37d584476aecfc36a6925e27a17c14a03dd89484bcc42f9beaa`  
		Last Modified: Fri, 07 Oct 2022 23:22:40 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
