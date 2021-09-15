## `openjdk:18-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:281e7ab9c66131fb0614dc381b79a7d2609ba9109021f673c28d029e88800fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `openjdk:18-ea-jdk-nanoserver-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull openjdk@sha256:cb149ca4d144cf4301c3987d5fcbe1eecbc3b80411b62bc91d8ad33d0e9dcfea
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288913526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46f3f183bb76afa05bb163f7c2d5280ff284bb380575933a2dcfb6a6abd2396`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 00:38:23 GMT
SHELL [cmd /s /c]
# Wed, 15 Sep 2021 00:38:24 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 15 Sep 2021 00:38:25 GMT
USER ContainerAdministrator
# Wed, 15 Sep 2021 00:38:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 15 Sep 2021 00:38:37 GMT
USER ContainerUser
# Wed, 15 Sep 2021 00:38:38 GMT
ENV JAVA_VERSION=18-ea+14
# Wed, 15 Sep 2021 00:38:54 GMT
COPY dir:51ec0ce7b7c9e4769d7449904cf647c2d5b50d722590d244bc3895b10447fd31 in C:\openjdk-18 
# Wed, 15 Sep 2021 00:39:06 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 15 Sep 2021 00:39:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:807d06303c39b2317729754a4c7ad6501e59c16ee464f8f671f9947774f62f72`  
		Last Modified: Wed, 15 Sep 2021 01:10:56 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353abb4dcfd1456117623d23e4be07d7d5c9e18c7ddea8dfb6225f99efa904b9`  
		Last Modified: Wed, 15 Sep 2021 01:10:55 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6beb0bff60eb1dfb88e1010454b9aaf8f176f0d004a94fefdedb88d8e7e2a4`  
		Last Modified: Wed, 15 Sep 2021 01:10:55 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bcb79c10ca3fae0a02ab85be6ab15af3a4ac4d7a0b8b54fd7a9c12cdd0b203`  
		Last Modified: Wed, 15 Sep 2021 01:10:55 GMT  
		Size: 75.1 KB (75126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57b1aff54bbfc95746d48fc4f9d9afbb2f1f02e7d7006d7a7d6265ae52f9289`  
		Last Modified: Wed, 15 Sep 2021 01:10:52 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e45cc6773dbbbbe0dbd7da9341a1ba0d5366e96ca2302f2a655de3c4f93582c`  
		Last Modified: Wed, 15 Sep 2021 01:10:52 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5834832ae9e60b2879623f4f905b8e13cdf7b77b791531895644a7a116cb371`  
		Last Modified: Wed, 15 Sep 2021 01:14:00 GMT  
		Size: 182.6 MB (182609374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac02d068211bb1be8482acea4b7815f3980b8bf68829aef46b9edcce169ee303`  
		Last Modified: Wed, 15 Sep 2021 01:10:53 GMT  
		Size: 3.5 MB (3518898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a583850df5fb82388de02b49c12664910a8b6df4eb38d1af348405d2ae9acecd`  
		Last Modified: Wed, 15 Sep 2021 01:10:52 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
