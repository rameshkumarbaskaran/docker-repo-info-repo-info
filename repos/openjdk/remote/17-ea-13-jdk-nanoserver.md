## `openjdk:17-ea-13-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:05b6ed4ad20b05b304813c079439fb821d6d4326b24ca3a405613dc57c0e3822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `openjdk:17-ea-13-jdk-nanoserver` - windows version 10.0.17763.1817; amd64

```console
$ docker pull openjdk@sha256:14078ae7aec78b961245af303cc2edcda61c7c3920e89f107888f39feb2fc18d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286080471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8faa002036f71d3b9803c15e57a9919ed00448bd79433a153248b252b30f362`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 26 Feb 2021 16:47:31 GMT
RUN Apply image 1809-amd64
# Wed, 10 Mar 2021 17:50:47 GMT
SHELL [cmd /s /c]
# Wed, 10 Mar 2021 17:50:48 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Mar 2021 17:50:49 GMT
USER ContainerAdministrator
# Wed, 10 Mar 2021 17:51:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Mar 2021 17:51:08 GMT
USER ContainerUser
# Thu, 11 Mar 2021 23:51:41 GMT
ENV JAVA_VERSION=17-ea+13
# Thu, 11 Mar 2021 23:51:57 GMT
COPY dir:32266cf532becbea71ec4d191b42af619fca19641748fcd6d3eb802c219b6117 in C:\openjdk-17 
# Thu, 11 Mar 2021 23:52:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 11 Mar 2021 23:52:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a11c4ca8f1ba16b6e1395d4523be2215bd0871c2e3e4695b9f2b87bd7472be52`  
		Size: 101.4 MB (101389964 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b1146273d9b624ee892dfcbb3c753523f09f79536a16d63b711cb0027825374a`  
		Last Modified: Wed, 10 Mar 2021 18:33:51 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c1ac1e6f2d0594fe7e8e0395310c60461fc8ce5183f6a15db964a07b66176e`  
		Last Modified: Wed, 10 Mar 2021 18:33:51 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050de60c3748a5bfc798f599cadba652e52a162ca31f36b8c783664c11ed224b`  
		Last Modified: Wed, 10 Mar 2021 18:33:54 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e309359702f2d5c4fa7bc854144ad320712050892d017cdfcb58acff4fea2609`  
		Last Modified: Wed, 10 Mar 2021 18:33:50 GMT  
		Size: 66.6 KB (66576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97ecf2dccedb4699a8caf6c19a7a80768c90efb0af5959f1465b00abe8faa12`  
		Last Modified: Wed, 10 Mar 2021 18:33:48 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bb37f6fac76fbe7edc033e05973af4a708faf6c238ce10f6345b177ea04fb4`  
		Last Modified: Fri, 12 Mar 2021 00:00:51 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bd2f68bd2a22ce733eaebef5c0f9a4ae9cc325756873b0b3e7978b301dbb95`  
		Last Modified: Fri, 12 Mar 2021 00:01:11 GMT  
		Size: 181.0 MB (180986665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d1b439b6995c36935b3e020cb912988d847e36dbc1d7f60807c2c6797e2c0c`  
		Last Modified: Fri, 12 Mar 2021 00:00:52 GMT  
		Size: 3.6 MB (3630538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ca0cc668cbd5d5bb00e2e8ca353da090ac31592aa89ed15d61d225131610c7`  
		Last Modified: Fri, 12 Mar 2021 00:00:51 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
