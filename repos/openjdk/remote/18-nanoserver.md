## `openjdk:18-nanoserver`

```console
$ docker pull openjdk@sha256:1874f8a1b923a4c82c4ed098c212cb58233fa6cc6b2a9b7ed12d40b82eb75276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `openjdk:18-nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull openjdk@sha256:68a6182c8e47bfe177d3cb2996539aff7ff00bc5c93e79e261a32e69c006eff0
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290243847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68e55517d281b97a6862a1090ec56e6fe65bb54d76e9a8c436eadc504a1ff43`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:13:20 GMT
SHELL [cmd /s /c]
# Wed, 10 Nov 2021 20:31:55 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 10 Nov 2021 20:31:55 GMT
USER ContainerAdministrator
# Wed, 10 Nov 2021 20:32:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Nov 2021 20:32:07 GMT
USER ContainerUser
# Fri, 10 Dec 2021 22:20:03 GMT
ENV JAVA_VERSION=18-ea+27
# Fri, 10 Dec 2021 22:20:19 GMT
COPY dir:57980dafd83f850a53416aef9f3889dd71bef73fc8ea0b8ccf11eaf766be5866 in C:\openjdk-18 
# Fri, 10 Dec 2021 22:20:45 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 10 Dec 2021 22:20:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e60ec86b90e1492e0e0ed2cbebcf624990a34862e24207343fd85b84b3544c8e`  
		Last Modified: Wed, 10 Nov 2021 18:01:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d97d878bac5dd9dcbe1bb5f45ade2111fc77e8d4a5a348163bd9c3ddddbaf0`  
		Last Modified: Wed, 10 Nov 2021 21:11:37 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5a46fd95d3a8e8b5949c49cc0d70b858bddbe38c8c33e0a6a3e0f157d7795a`  
		Last Modified: Wed, 10 Nov 2021 21:11:37 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88539ad3f1fb0ea6957da9a7298c1f6546afbb52b2deb7199763195fca993d98`  
		Last Modified: Wed, 10 Nov 2021 21:11:37 GMT  
		Size: 74.2 KB (74205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d133fe2173015750539b2d0a8fb86dbdbe0c6b44c8d75ddeb714a82814f98e00`  
		Last Modified: Wed, 10 Nov 2021 21:11:33 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f009d518c920db4649bb4a3b9e1988ea0a68b02983c9688da14f7dffb19e347a`  
		Last Modified: Fri, 10 Dec 2021 22:30:50 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d881716db25ecb4f2bd4213b50d8d0ebae4f926821a9140080b61eee7afcda4f`  
		Last Modified: Fri, 10 Dec 2021 22:31:09 GMT  
		Size: 183.9 MB (183862277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691abbc201ee8d7092c49ea0602eae17b4a64f0629e7b22d50ba9ca573459729`  
		Last Modified: Fri, 10 Dec 2021 22:30:51 GMT  
		Size: 3.5 MB (3517766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beda7192637fe7650be1ddd0eae9f582e43247c4cd26dd45ee9374fe7018888a`  
		Last Modified: Fri, 10 Dec 2021 22:30:50 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
