## `openjdk:20-ea-nanoserver`

```console
$ docker pull openjdk@sha256:a0cebba74498db2ecde3b84ec49826d31f422583235d1d9ded01a6565a71a51a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `openjdk:20-ea-nanoserver` - windows version 10.0.17763.3532; amd64

```console
$ docker pull openjdk@sha256:aaef338191b6ed6bdad7a56c8759e6739c426da161a21ffd45e89e0d9143c505
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303842074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2222c9fd76982804847888be117befbb43933e74b60c13e63138702b9bad5b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Wed, 12 Oct 2022 15:20:49 GMT
SHELL [cmd /s /c]
# Wed, 12 Oct 2022 16:43:51 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 12 Oct 2022 16:43:51 GMT
USER ContainerAdministrator
# Wed, 12 Oct 2022 16:44:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 Oct 2022 16:44:03 GMT
USER ContainerUser
# Thu, 27 Oct 2022 21:18:50 GMT
ENV JAVA_VERSION=20-ea+21
# Thu, 27 Oct 2022 21:19:06 GMT
COPY dir:f087053ae704e5f0e8d3a363b43872069ef7f16f6f376486d85a02a4d6564318 in C:\openjdk-20 
# Thu, 27 Oct 2022 21:19:31 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 27 Oct 2022 21:19:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ce29f4214f0fb0200b149c387d5e94ee47d5705e9bc7b884331390782282065f`  
		Last Modified: Thu, 27 Oct 2022 21:23:38 GMT  
		Size: 106.8 MB (106773776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6a667d76c19fca171390d60fb90c40e16c777050e943a7fe17ad7686841f0f`  
		Last Modified: Wed, 12 Oct 2022 16:02:59 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4315d417eb7958a05c7977d0ea6b1b4745e46725d02f23235173bbad2c73101d`  
		Last Modified: Wed, 12 Oct 2022 16:53:09 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c783713d738fc9dfff161ad3ff4369333cd0881466ab886feb09e6ef3508512e`  
		Last Modified: Wed, 12 Oct 2022 16:53:09 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05686fefb2145f84031cd9cae616dd90496d078df87f19c080931972eb700e7c`  
		Last Modified: Wed, 12 Oct 2022 16:53:09 GMT  
		Size: 67.2 KB (67186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab8462cae193737dba91e48900abf79d1b7234b48f337497ae0abfe9d8189e5`  
		Last Modified: Wed, 12 Oct 2022 16:53:07 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01eebc0ffc84d5253b5f527e4d9be8a67c5b660550c2aca2f54695519b7dbd8c`  
		Last Modified: Thu, 27 Oct 2022 21:22:56 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5714b40f8e1e528053d18866904d49b907ed02e316aa62b0c5b6fe95cd1c68`  
		Last Modified: Thu, 27 Oct 2022 21:23:24 GMT  
		Size: 193.2 MB (193212247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84293dee62116522c99f271d8e2338a4913118268614a9ca6619d7083f257a7`  
		Last Modified: Thu, 27 Oct 2022 21:22:57 GMT  
		Size: 3.8 MB (3781891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bea2a1e3b722d647cda70c9c20881356d2badc0b0e63218cfeb0448bd27fbd`  
		Last Modified: Thu, 27 Oct 2022 21:22:56 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
