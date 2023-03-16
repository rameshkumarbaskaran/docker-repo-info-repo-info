## `openjdk:20-rc-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:520bb92baef9529fcbeb5c701f5e853bc5ee52def8f00f9eb2162f259e36e554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `openjdk:20-rc-jdk-nanoserver` - windows version 10.0.17763.4131; amd64

```console
$ docker pull openjdk@sha256:d9cd2f4f03360e370077f8df4eb5ef45e5e7c8d0995685d71f2d75935dcc41b7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303604188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb98610dd1509d069a2c452a135e914f01f7f0fd81d767cd7b7b31d8094bdab`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 00:45:50 GMT
SHELL [cmd /s /c]
# Thu, 16 Mar 2023 04:28:34 GMT
ENV JAVA_HOME=C:\openjdk-20
# Thu, 16 Mar 2023 04:28:35 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 04:28:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 16 Mar 2023 04:28:49 GMT
USER ContainerUser
# Thu, 16 Mar 2023 04:28:50 GMT
ENV JAVA_VERSION=20
# Thu, 16 Mar 2023 04:29:07 GMT
COPY dir:993cb869459fba742419cffbcf553ece0591a50d69cbcdfd0aea8e998cf9d7ec in C:\openjdk-20 
# Thu, 16 Mar 2023 04:29:33 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 16 Mar 2023 04:29:34 GMT
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
	-	`sha256:64380c9482d5f81cf0626bbfc423fccf06aac281f0d9cdea678f83a081c575b6`  
		Last Modified: Thu, 16 Mar 2023 04:34:11 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af15f48a225441315f60883c71211fa38f133da33c54f0e6624f48cd676e52bd`  
		Last Modified: Thu, 16 Mar 2023 04:34:11 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2073a736bf0260df5d9e9068a5102e976285abe4304961b03add39c168984f2`  
		Last Modified: Thu, 16 Mar 2023 04:34:11 GMT  
		Size: 70.7 KB (70683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2719b6b7ae4f2e1485ce76cb3f78a41cd56de1a88f04978ddd525a0342ca2a8`  
		Last Modified: Thu, 16 Mar 2023 04:34:09 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7a1b93c246120873a7b84025385bc08ae0535cf902fddee7c392aee7b2d72b`  
		Last Modified: Thu, 16 Mar 2023 04:34:08 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc93bdfcf2f58f9bfab9e22af485bb97c49d80941673d28c5b1f71d7bf01b03`  
		Last Modified: Thu, 16 Mar 2023 04:34:34 GMT  
		Size: 193.1 MB (193065662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0509d3abed8de9b0bb2c220c38326dd965e5d2127b8aea9e39aebf5cac5b515`  
		Last Modified: Thu, 16 Mar 2023 04:34:10 GMT  
		Size: 3.8 MB (3776773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28ac7ee327bf80e8d1c074b102a496b30b7cd1f31c516c8df02171c692dadea`  
		Last Modified: Thu, 16 Mar 2023 04:34:09 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
