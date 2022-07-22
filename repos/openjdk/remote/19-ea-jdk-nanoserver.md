## `openjdk:19-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:a7d949a1529e48c3bb2dac9eb3a40732c17b5aea1c497981f1f7d94f69dbe32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `openjdk:19-ea-jdk-nanoserver` - windows version 10.0.17763.3165; amd64

```console
$ docker pull openjdk@sha256:561c575e09f1a8984ef5e0a226bc6f33bdb1d2846ebecfb7a206caad209fe903
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298156972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3100a39a83416415e63d385304fd71b240e70f1b6336352fd0addba5c26a1a74`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:50:41 GMT
SHELL [cmd /s /c]
# Wed, 13 Jul 2022 15:57:38 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 13 Jul 2022 15:57:39 GMT
USER ContainerAdministrator
# Wed, 13 Jul 2022 15:57:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 Jul 2022 15:57:47 GMT
USER ContainerUser
# Thu, 21 Jul 2022 23:21:53 GMT
ENV JAVA_VERSION=19-ea+32
# Thu, 21 Jul 2022 23:22:07 GMT
COPY dir:f353c34b74dfb886c0a48fb5f30132cd9f7b097680a91f945a51af9d15023827 in C:\openjdk-19 
# Thu, 21 Jul 2022 23:22:24 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 21 Jul 2022 23:22:24 GMT
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
	-	`sha256:a24a8dc780930fe59a9967fb76b10b2fb2ac36ff76c3697586a3df823f25ab8d`  
		Last Modified: Mon, 18 Jul 2022 21:24:44 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1582b9bf63a2d6ede0a45ecb506c093cf9a09b81e8de25dd46c5bffa9c7d94`  
		Last Modified: Mon, 18 Jul 2022 21:24:43 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4239363179c317c462b5006da97ce6faa8c7e4256719a99f4c3dd0cb7a4b524f`  
		Last Modified: Mon, 18 Jul 2022 21:24:43 GMT  
		Size: 69.0 KB (69030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262dd52e79d9b5ebce7877fd3f3e42eb3c3cfae509d375aa166c3a01cb8e29a9`  
		Last Modified: Mon, 18 Jul 2022 21:24:41 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9146077a9f2eea20dbda3a7411e2d5ea08fce4eddf2ba3fa3e221719bb5bf3`  
		Last Modified: Thu, 21 Jul 2022 23:30:23 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48bfa156ca33df1e62c30d26a5ca15b74b2b6418897455b9a92fdeb6ab6aae9`  
		Last Modified: Thu, 21 Jul 2022 23:30:44 GMT  
		Size: 191.2 MB (191195827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b981d5cf91e07b5f95db65e1bcd59fca278d357363c45ac2c777d7d476e19378`  
		Last Modified: Thu, 21 Jul 2022 23:30:24 GMT  
		Size: 3.7 MB (3730530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d6b67fbea2f3cf05e177af56390cd55b62983ef3833505cddb2eab0cf8cd91`  
		Last Modified: Thu, 21 Jul 2022 23:30:23 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
