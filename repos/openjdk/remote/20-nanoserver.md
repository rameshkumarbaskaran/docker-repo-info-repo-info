## `openjdk:20-nanoserver`

```console
$ docker pull openjdk@sha256:4ac5f9f9625514cca2bbefead85177b29da5d90adea3fb27f4da53a5a3e31ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `openjdk:20-nanoserver` - windows version 10.0.17763.3165; amd64

```console
$ docker pull openjdk@sha256:daa531af9037cbbe725a92d15e92132c2b406fcee44df3320d0ad76d1f3f9831
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.2 MB (299175215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7587a38cd95ed2d0be804ee637cc43ea6761d8be30d9fa4018559caa2f298b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:50:41 GMT
SHELL [cmd /s /c]
# Wed, 13 Jul 2022 15:52:36 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 13 Jul 2022 15:52:37 GMT
USER ContainerAdministrator
# Wed, 13 Jul 2022 15:52:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 Jul 2022 15:52:50 GMT
USER ContainerUser
# Thu, 21 Jul 2022 23:18:10 GMT
ENV JAVA_VERSION=20-ea+7
# Thu, 21 Jul 2022 23:18:26 GMT
COPY dir:c69db79da21cce10e394e0f9d1458195cabf2a0dbf2acead5c9e403b3c04ae54 in C:\openjdk-20 
# Thu, 21 Jul 2022 23:18:52 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 21 Jul 2022 23:18:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b09c07c6aeead64423fdefc240fe2e1b6330c96732fd2705113030da84416be`  
		Last Modified: Mon, 18 Jul 2022 21:22:33 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c94d05d6baacbfa68cfb2958f0965811612f86860a0e4f86c3742cdbfbc022`  
		Last Modified: Mon, 18 Jul 2022 21:22:32 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cae155d737666fa6fb6c74f820b3e7f2470d72055ea13febb624515fcec6e1f`  
		Last Modified: Mon, 18 Jul 2022 21:22:32 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf301cbd6754860321dd411bf1baa15e0ba0f68154452e0ffb84915c2340f3f`  
		Last Modified: Mon, 18 Jul 2022 21:22:32 GMT  
		Size: 73.1 KB (73119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb02d029b4db33c144b7edd2594c5c7df303b1ea68bf6135d5133634b910d307`  
		Last Modified: Mon, 18 Jul 2022 21:22:30 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1685047209692abc8d194ddb98aabe4de697c3c34a7f130a4d9e7d5f0b25e126`  
		Last Modified: Thu, 21 Jul 2022 23:28:20 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e273e7cea348da0a694783bb261c77cb2581e1df6bcf483bca8b1134b4d04d2`  
		Last Modified: Thu, 21 Jul 2022 23:28:41 GMT  
		Size: 192.2 MB (192233053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26290846af9ca8e3c89dc8f28d6a25c26398066fc4b33a87aa44caa9fbec88f`  
		Last Modified: Thu, 21 Jul 2022 23:28:21 GMT  
		Size: 3.7 MB (3707332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d7c11e5faa31ae850f27414150252c18b817ea25043735a27c4555093421f0`  
		Last Modified: Thu, 21 Jul 2022 23:28:20 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
