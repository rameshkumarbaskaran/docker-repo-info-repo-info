## `openjdk:21-ea-12-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:34514b052e4193e04d3e6f7dc2e5cb8a980ea6706db88bfdb4f0a6075b452300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `openjdk:21-ea-12-jdk-nanoserver` - windows version 10.0.17763.4010; amd64

```console
$ docker pull openjdk@sha256:e150b273485dc4b8fc7900ac524e325729d8cefa37de68bcaf020064e9919f12
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304842960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81f1b026714f244b57b7891e3f0a4b7144923d700f8fe6dbafac57a35c84810`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Feb 2023 10:14:28 GMT
RUN Apply image 10.0.17763.4010
# Wed, 15 Feb 2023 22:46:15 GMT
SHELL [cmd /s /c]
# Thu, 16 Feb 2023 02:20:16 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 16 Feb 2023 02:20:17 GMT
USER ContainerAdministrator
# Thu, 16 Feb 2023 02:20:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 16 Feb 2023 02:20:27 GMT
USER ContainerUser
# Sat, 04 Mar 2023 00:23:33 GMT
ENV JAVA_VERSION=21-ea+12
# Sat, 04 Mar 2023 00:23:50 GMT
COPY dir:1d679f21c78109dbcdb8a20dd946cf513cc3495e657ace8c1daf5090785fe2a4 in C:\openjdk-21 
# Sat, 04 Mar 2023 00:24:29 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 04 Mar 2023 00:24:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:00eaf3341cd3cc6b72f91399cb3bd1aba30eb7eead7596532fe54c4bf1b010d7`  
		Last Modified: Thu, 16 Feb 2023 00:31:21 GMT  
		Size: 106.7 MB (106674970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0185f49bd9e9c2d18b1dcf8f1f67123b4146383e07a158cb4623d96fb2d18c05`  
		Last Modified: Thu, 16 Feb 2023 02:29:16 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b040b2f53926e6a02088ae0173e36f1f01b75c581f435607dd2f86dfe095f4a`  
		Last Modified: Thu, 16 Feb 2023 02:29:16 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0134c2e5e080e208ed0917cd948446b60048729433bf731850e4165e426977c`  
		Last Modified: Thu, 16 Feb 2023 02:29:16 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf352af9ffad203bc10ae043af50fee20ca5c0e02a370dcc2b040c702c9d48f`  
		Last Modified: Thu, 16 Feb 2023 02:29:16 GMT  
		Size: 67.9 KB (67900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58adc24996cad294b1ceeed12449ee5750c4442dfcc5e3135984239942ba8503`  
		Last Modified: Thu, 16 Feb 2023 02:29:13 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984486a2a751e21502d45843b01e752e6393ff4a7d47bdd5422541d31b5821f1`  
		Last Modified: Sat, 04 Mar 2023 01:18:58 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b013f9053e2b7d2bb5f7750a21f7da3557c9f2c24abbe5ff5d07dbe69484b824`  
		Last Modified: Sat, 04 Mar 2023 01:19:20 GMT  
		Size: 194.3 MB (194292923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d15100543e52ebef7a0221022f89b91dbf988cade67acc301a134db335c405`  
		Last Modified: Sat, 04 Mar 2023 01:18:59 GMT  
		Size: 3.8 MB (3800323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a2514cdd650884def66cb84319728ea2eb9963b4716a01f628e023b6df15fd`  
		Last Modified: Sat, 04 Mar 2023 01:18:58 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
