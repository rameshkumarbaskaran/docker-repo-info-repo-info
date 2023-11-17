## `openjdk:22-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:0c0b97e9257365ec694c06f4ebf665c661342120bacbb8d27e7018e46e4af850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `openjdk:22-jdk-nanoserver-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull openjdk@sha256:98d9ec1282b455168d2159258e3027ef3001853486ff83a2d8e6f79cf4e2264d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.3 MB (307311878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ecf3883f3268319ae5eb0afdb6a38e6b280ec9549e96b8c02f3b285acaa050`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 01:41:12 GMT
SHELL [cmd /s /c]
# Thu, 16 Nov 2023 05:24:44 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 16 Nov 2023 05:24:45 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 05:24:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 16 Nov 2023 05:24:56 GMT
USER ContainerUser
# Fri, 17 Nov 2023 02:19:09 GMT
ENV JAVA_VERSION=22-ea+24
# Fri, 17 Nov 2023 02:19:24 GMT
COPY dir:fb5c10b10e4eed2b9a0b6857b6fe9ac81afcde1151f63d6158ef6390c04bccda in C:\openjdk-22 
# Fri, 17 Nov 2023 02:19:41 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 17 Nov 2023 02:19:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e5c133738aab79d4c21c47e77cb838e2d00166f5e3e2632177622f67488259`  
		Last Modified: Thu, 16 Nov 2023 02:28:08 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d4362f257916ef69830b46ba8a0aacd5f6e2d4673fbd0dd7e4aac8cf3a6fb4`  
		Last Modified: Thu, 16 Nov 2023 05:27:30 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbc097ffc72e1215bdcee71d660b96a870a6af75ff16317f8a06d1555574aaa`  
		Last Modified: Thu, 16 Nov 2023 05:27:30 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765165baea11820cc78dbfb0922d099fef71e3cab0a77276be9bf3096bc3d841`  
		Last Modified: Thu, 16 Nov 2023 05:27:30 GMT  
		Size: 73.6 KB (73582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279359aca9bd1c2c8d38ba732e66b1a8948268dbc2347c4add167c46cc62574c`  
		Last Modified: Thu, 16 Nov 2023 05:27:28 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6cc343ba449375433ad5bc909b70875920d69a531434c61d972a437e375b68`  
		Last Modified: Fri, 17 Nov 2023 02:21:43 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b4db38b699db71ab0e1a36b362d18cb7a60f33ac7fb0e663efc3c7467d93d6`  
		Last Modified: Fri, 17 Nov 2023 02:22:03 GMT  
		Size: 198.9 MB (198930154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10508815e354733ffa517922b34dbc1389e653691458053b68a7f9a7c646feb`  
		Last Modified: Fri, 17 Nov 2023 02:21:45 GMT  
		Size: 3.8 MB (3803800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649cff34e9a140294f9940aeb9ec16442063ebc2b11bb26b59d95601045917db`  
		Last Modified: Fri, 17 Nov 2023 02:21:43 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
