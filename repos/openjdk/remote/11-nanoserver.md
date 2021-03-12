## `openjdk:11-nanoserver`

```console
$ docker pull openjdk@sha256:d02decc8b4b20a036b1f880abb261e59ccd28e57ac288281a4b7a7b8815237b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `openjdk:11-nanoserver` - windows version 10.0.17763.1817; amd64

```console
$ docker pull openjdk@sha256:4183c1bac02bfefbc9848f7e405f1e4e2f15603694d5ce2913f63b1576d7ba96
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292406001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc00372ab08903b6803cd3f744d22b1320f5aa23161d1f449a7c9ac56a29c01f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 26 Feb 2021 16:47:31 GMT
RUN Apply image 1809-amd64
# Wed, 10 Mar 2021 17:50:47 GMT
SHELL [cmd /s /c]
# Wed, 10 Mar 2021 18:11:04 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Mar 2021 18:11:04 GMT
USER ContainerAdministrator
# Wed, 10 Mar 2021 18:11:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Mar 2021 18:11:18 GMT
USER ContainerUser
# Wed, 10 Mar 2021 18:11:19 GMT
ENV JAVA_VERSION=11.0.10
# Wed, 10 Mar 2021 18:11:38 GMT
COPY dir:c55c8a7ac9bf87302336a84fe1caa0b79ec42696e5d6969bc177cd9d6262fe26 in C:\openjdk-11 
# Wed, 10 Mar 2021 18:11:57 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 10 Mar 2021 18:11:58 GMT
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
	-	`sha256:26e688e0214a8f608710f492cdcc700b975b72c2672384c69af59e23cd64cf03`  
		Last Modified: Wed, 10 Mar 2021 18:48:16 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936b244874d855fd95d08bc3148609392dcfa59bd7eb38794d14f6a8acfe843a`  
		Last Modified: Wed, 10 Mar 2021 18:48:16 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e52635132491e5431ac0c66493b2fb3e11e92a4e1c96f3a620c30eaad9e2c6`  
		Last Modified: Wed, 10 Mar 2021 18:48:17 GMT  
		Size: 67.6 KB (67586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90cfe91b7222842f96fad2c2fbfe20dd858a3ee05df26a9c09fbb6746f76e96`  
		Last Modified: Wed, 10 Mar 2021 18:48:14 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d7988aeb14c3d048adefaacb8f4babc8dc43e391745b2adef8e340d67ef016`  
		Last Modified: Wed, 10 Mar 2021 18:48:15 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf012b9db76cc1e4fa65533c74d1364d72de49002f909a3d621e6107c787f95`  
		Last Modified: Wed, 10 Mar 2021 18:48:44 GMT  
		Size: 190.9 MB (190850689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cbe5f70cda8d5d5a08c7dc1a3b02946a7562985dc922842d9e0575a2fb0143`  
		Last Modified: Wed, 10 Mar 2021 18:48:14 GMT  
		Size: 90.7 KB (90740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e82c9c0dd310332c72d8600c63023e3b5995d2c97904a4ea58d3792340c49e`  
		Last Modified: Wed, 10 Mar 2021 18:48:14 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
