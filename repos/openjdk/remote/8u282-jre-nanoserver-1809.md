## `openjdk:8u282-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:9ac37e80333be795fae7ef164e95216f18238fa5a337e458d0e595965b7535eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `openjdk:8u282-jre-nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull openjdk@sha256:a12e68de288a83e3f3650ccd484aac849c28272cef88489c4e5772306a91a4dd
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139693421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352d7a1ac0b8257748eef46ee46f26273d143c8fa8706cd60d7509bd89838877`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:53:40 GMT
SHELL [cmd /s /c]
# Wed, 14 Apr 2021 17:27:30 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 Apr 2021 17:27:31 GMT
USER ContainerAdministrator
# Wed, 14 Apr 2021 17:27:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Apr 2021 17:27:45 GMT
USER ContainerUser
# Wed, 14 Apr 2021 17:27:46 GMT
ENV JAVA_VERSION=8u282
# Wed, 14 Apr 2021 17:31:33 GMT
COPY dir:f51b6315789fea62bc81073100310d85cf4082234fc7f3bd9b51f6f4a883a8f3 in C:\openjdk-8 
# Wed, 14 Apr 2021 17:31:51 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c2c727299531adc7c2aacb1f062d72fd42cec96a0d235b3e5b0afe03e9ddbc7d`  
		Last Modified: Wed, 14 Apr 2021 17:41:13 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c7d921929195146d6442e27a405dc06676d7e52a8806c1041a8a821b3ae91d`  
		Last Modified: Wed, 14 Apr 2021 17:54:28 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d17b71c3462fefa5234492d0bc83528577a7de4432da7075bee4accc63546d8`  
		Last Modified: Wed, 14 Apr 2021 17:54:27 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a3200fb343c477ec4976a94e9ad98dee760d79fc21d4bfc39becf564ff377a`  
		Last Modified: Wed, 14 Apr 2021 17:54:25 GMT  
		Size: 66.2 KB (66240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84869171477acabf60cdc0f43e92b340759190808d1e93844a909b9f45d2062`  
		Last Modified: Wed, 14 Apr 2021 17:54:25 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606798ecdb337502582400700729fd7b553663ef0301fd594f1fd7d398ce5ac7`  
		Last Modified: Wed, 14 Apr 2021 17:54:25 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb59e54326afb3d79b63fa30d14481deadc61ba10c896f8b87161911ed639cd`  
		Last Modified: Wed, 14 Apr 2021 17:56:31 GMT  
		Size: 38.2 MB (38199040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baefe218c79569e3326089abcf7cb0700e785bbb6c9b887559d707635473950f`  
		Last Modified: Wed, 14 Apr 2021 17:56:23 GMT  
		Size: 82.4 KB (82442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
