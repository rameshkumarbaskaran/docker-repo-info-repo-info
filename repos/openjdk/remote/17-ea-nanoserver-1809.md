## `openjdk:17-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:46ec6676a3aaeb484c9b3ff6c4da9e904ef3c1000886faf1b76a619b9981f94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:17-ea-nanoserver-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:a767d663be44ef82d2b9bf37ba7d8403850af6b6c27c5d1a41da8caaf1aa2f26
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286127757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2dbb96b7e3a73ecd872c8a6f5b73daebcae697a0258abd0bcb454cab26c7c2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:56:48 GMT
SHELL [cmd /s /c]
# Wed, 13 Jan 2021 19:56:48 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 13 Jan 2021 19:56:49 GMT
USER ContainerAdministrator
# Wed, 13 Jan 2021 19:57:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 13 Jan 2021 19:57:07 GMT
USER ContainerUser
# Sat, 23 Jan 2021 01:19:57 GMT
ENV JAVA_VERSION=17-ea+6
# Sat, 23 Jan 2021 01:20:28 GMT
COPY dir:6c9f867619c706d4cf35eeb1b6bc4b5fb5354ed0271c18b096608ebd209a7a7e in C:\openjdk-17 
# Sat, 23 Jan 2021 01:20:48 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Sat, 23 Jan 2021 01:20:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c2b6c001c337f812bceb3b03d15a70d1d9905540658e751e42f20f7cc0ddc819`  
		Last Modified: Wed, 13 Jan 2021 21:16:47 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788a0bd344d2eb3850ddd4570305cbcf959de9a743a310f941c297081c240d8f`  
		Last Modified: Wed, 13 Jan 2021 21:16:46 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db311194c9cbd0c67151ee177949a18a7ad83e5551b659b30ef3151062c5a98`  
		Last Modified: Wed, 13 Jan 2021 21:16:47 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a588d5e7e84f7b20f460bb66a5bb1f2b7e762713923669ac453e6eda8b23eb7`  
		Last Modified: Wed, 13 Jan 2021 21:16:44 GMT  
		Size: 68.0 KB (68013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df625a811b1b58029fb5e4c987218865063cb248bd9d163cc15c8584c8af7afd`  
		Last Modified: Wed, 13 Jan 2021 21:16:40 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f174830ddbb355442e97d83c3c9996780fd01ce14c225460f6066b0ee4e46a`  
		Last Modified: Sat, 23 Jan 2021 01:36:15 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cc49c1c6cb362ccfd5b607bf5c5d36fd35526caf2e1d808c5823369e1303c7`  
		Last Modified: Sat, 23 Jan 2021 01:36:34 GMT  
		Size: 181.0 MB (181004584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e18638637008343c1ab30c1db7e87c54d66ca9214ffee5744f7080458363d9`  
		Last Modified: Sat, 23 Jan 2021 01:36:19 GMT  
		Size: 3.7 MB (3709387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8571cf45597510e33dc8dcb17c401372f26de38954e2db8fa0853786aeaf4fe8`  
		Last Modified: Sat, 23 Jan 2021 01:36:15 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
