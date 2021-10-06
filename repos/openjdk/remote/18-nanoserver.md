## `openjdk:18-nanoserver`

```console
$ docker pull openjdk@sha256:0a76cd852dd9fbb450ddbaa689fb0b80119ea75eda7d9ed8bc0ff4358945eb38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `openjdk:18-nanoserver` - windows version 10.0.17763.2183; amd64

```console
$ docker pull openjdk@sha256:6557bc694f62ec27bb51a053aec81790e0dc31ff8d233e054b9093e9b5527aa6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289388098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa02bc1116858b640d5ecb52f90aca1494f4a84aef580ca4c78dc2164242bc1f`
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
# Wed, 06 Oct 2021 18:18:08 GMT
ENV JAVA_VERSION=18-ea+17
# Wed, 06 Oct 2021 18:18:27 GMT
COPY dir:f356b3394c4a075d95af45ffe1916e24e012325a546f72fc0d3c27a71902e227 in C:\openjdk-18 
# Wed, 06 Oct 2021 18:18:48 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 06 Oct 2021 18:18:49 GMT
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
	-	`sha256:462330f839616bf3fc26d465c074f9a417dd7ad59b63b6f962eedb2b9a9ee4f0`  
		Last Modified: Wed, 06 Oct 2021 19:24:32 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02407481d803b023394ad2a1cdc81c0ed0a3e3124e716632a8214b3dcf861999`  
		Last Modified: Wed, 06 Oct 2021 19:27:51 GMT  
		Size: 183.1 MB (183071015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b2fcd31335a5343a5b879ab94494367a0f5d8526c5e3c71daec45a0cbbb36f`  
		Last Modified: Wed, 06 Oct 2021 19:24:33 GMT  
		Size: 3.5 MB (3531595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4d5875460c46a3cbbcfadce6e103453eaf14bd15c99b05701e21c4fed36b44`  
		Last Modified: Wed, 06 Oct 2021 19:24:32 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
