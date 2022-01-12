## `openjdk:19-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:3a9723700c5347edc6d65eed690100a2de36b634fa1dd8e1f8f76be59369a1c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `openjdk:19-ea-jdk-nanoserver` - windows version 10.0.17763.2452; amd64

```console
$ docker pull openjdk@sha256:6076a60369de118e480a45e961f2ae2eead2a99da23e75939a11543e15af9811
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291473912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877f23c39d056ed6012b59ed2da22067af874d5371c3b966cbe072a128d41e66`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 05:19:56 GMT
SHELL [cmd /s /c]
# Wed, 12 Jan 2022 05:19:57 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 12 Jan 2022 05:19:57 GMT
USER ContainerAdministrator
# Wed, 12 Jan 2022 05:20:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 Jan 2022 05:20:11 GMT
USER ContainerUser
# Wed, 12 Jan 2022 05:20:12 GMT
ENV JAVA_VERSION=19-ea+4
# Wed, 12 Jan 2022 05:20:40 GMT
COPY dir:0e17b3361127d84da6697596100040ca0746296f166480523a243817ad096d15 in C:\openjdk-19 
# Wed, 12 Jan 2022 05:20:57 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 12 Jan 2022 05:20:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:71dcb756adb8534a87210067788d6aa4a5a366b72d022b7af035e5263a3e54a0`  
		Last Modified: Wed, 12 Jan 2022 16:05:17 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd7300b4019ff9b559340d01ecbd3d68b9dd33c2df25033ff796154aec89a49`  
		Last Modified: Wed, 12 Jan 2022 23:01:27 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dac77d42d3ecdfc24be65cecefec26e9e433a99fe6148cec310fe5034c9f82e`  
		Last Modified: Wed, 12 Jan 2022 23:01:27 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa17938ac81d5b8ee2d1f4641d9497bd986cb5c96781c42505926d98415fae9a`  
		Last Modified: Wed, 12 Jan 2022 23:01:26 GMT  
		Size: 68.1 KB (68132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae12b4a1b26fd286c13ce523fa51853cdb24bb42fb4251ba9b9e175bb6723305`  
		Last Modified: Wed, 12 Jan 2022 23:01:24 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292c9e43ba0dea184c84fb3b851e1026bde029fd4af46926151a3c5ddda72297`  
		Last Modified: Wed, 12 Jan 2022 23:01:24 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1f8f8cfcf6f21cbaae227cc72e66406796a0c88e8fd161db33520b9d32bd16`  
		Last Modified: Wed, 12 Jan 2022 23:01:46 GMT  
		Size: 184.8 MB (184819797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c0e89f1e510946fdb5a5dee3ac9fc9bbf5edd5af0b5b95bbea8b6789fa436e`  
		Last Modified: Wed, 12 Jan 2022 23:01:28 GMT  
		Size: 3.5 MB (3548056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86ca359b7a3d5bf806f4c7c8143a64aa963f5556cf1003051006579fb0a8165`  
		Last Modified: Wed, 12 Jan 2022 23:01:24 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
