## `openjdk:21-ea-13-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:76c31f85fe7cc25ff1414bd55e2164e458b5605a41445231e0ea3b6b3cd0ac67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `openjdk:21-ea-13-jdk-nanoserver-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull openjdk@sha256:9c19031a2209daf7bdd61e76e38bf954fef92788968948992c61bd97e54d5b10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304948495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d6e1ee36872e1c595a673e93607e5ba17e992fdb66f6a780c32e51e23b9c17`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 00:45:50 GMT
SHELL [cmd /s /c]
# Thu, 16 Mar 2023 04:21:31 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 16 Mar 2023 04:21:32 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 04:21:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 16 Mar 2023 04:21:45 GMT
USER ContainerUser
# Thu, 16 Mar 2023 04:21:46 GMT
ENV JAVA_VERSION=21-ea+13
# Thu, 16 Mar 2023 04:22:04 GMT
COPY dir:2075528fbfcbd8cb9dbdcc1eca298b0afad536273edb6ac4d6a9a87f315425a9 in C:\openjdk-21 
# Thu, 16 Mar 2023 04:22:31 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 16 Mar 2023 04:22:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5837fe68a36caddf38b0aaa99f4ef20ca36d8dfe2825fa6ffbcf0d38b9d59a`  
		Last Modified: Thu, 16 Mar 2023 01:42:43 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450d272e24dcd824ed0a2cfaab457791740701be7e655050f5a344dba0111120`  
		Last Modified: Thu, 16 Mar 2023 04:32:07 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375c9b367947b6469eed8f3b494a27778599dd1e8ab85682d96eee96a8d38097`  
		Last Modified: Thu, 16 Mar 2023 04:32:07 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d48b42b9c3192f6ddd8ce43c9c7a2c8b1fb3f906fe4eea3aa9b1e4fc28b4161`  
		Last Modified: Thu, 16 Mar 2023 04:32:08 GMT  
		Size: 72.2 KB (72190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44544dc6ee19ff5b39d3756cbc6d53830c65429f0d1ad05b8422c3c33ac8311`  
		Last Modified: Thu, 16 Mar 2023 04:32:05 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495d40d958c73015d145c95863901a85c52333698020c3d459376ff69fb43aa1`  
		Last Modified: Thu, 16 Mar 2023 04:32:05 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe525f0414a15fb5e8476d62517998f279ebddd1cf851402e54f5c9bd054e46e`  
		Last Modified: Thu, 16 Mar 2023 04:32:30 GMT  
		Size: 194.4 MB (194416171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e4ecb56fbab4a12178ecb8674582910ddcf865fc91c59ba05f3b720d0290b6`  
		Last Modified: Thu, 16 Mar 2023 04:32:06 GMT  
		Size: 3.8 MB (3768998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7342dbcc6a3137a17ea0ba6683d0c7ddb3b7185e5eaf02c402ae137fd8279d4c`  
		Last Modified: Thu, 16 Mar 2023 04:32:05 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
