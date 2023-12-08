## `openjdk:22-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:ab30f5ce0b30cf86424ff4c292b29cc4bc3e202caa29c906a5e128a8e228b638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `openjdk:22-ea-nanoserver-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull openjdk@sha256:035137d7b6fb0f1eb7cca8313d58a11d97ca50344cff50d1ce442c99bc525847
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.7 MB (305738599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b2f40a6865e742e907e1e06773a3af9a0636132f882f9dad5c7011c8108450`
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
# Fri, 08 Dec 2023 22:18:38 GMT
ENV JAVA_VERSION=22-ea+27
# Fri, 08 Dec 2023 22:18:52 GMT
COPY dir:ff057bf08d63776ecb0d546e093c8fd881ebaf7ac625535f56acbf65c5f8c473 in C:\openjdk-22 
# Fri, 08 Dec 2023 22:19:08 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 08 Dec 2023 22:19:08 GMT
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
	-	`sha256:af374330f11dc7f04127438ad91e869fd94a65873853ca0636d85bf992a65ce6`  
		Last Modified: Fri, 08 Dec 2023 22:21:06 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10faef5d10b3d9a9fa1b0c408c07b56b1e3fbe78901e531184bbf8f502533560`  
		Last Modified: Fri, 08 Dec 2023 22:21:25 GMT  
		Size: 197.4 MB (197355934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6499dd7c03a1701d1dbf9c544abbc2e5619e50d39848864ecb40d73724234995`  
		Last Modified: Fri, 08 Dec 2023 22:21:07 GMT  
		Size: 3.8 MB (3804737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93067b37a3abe0bd604007064f29d12062b915fb35f3c9ae6c991307fc5cf53`  
		Last Modified: Fri, 08 Dec 2023 22:21:06 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
