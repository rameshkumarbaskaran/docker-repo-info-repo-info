## `openjdk:8u282-nanoserver-1809`

```console
$ docker pull openjdk@sha256:91916c0318e751826243da99c0aeeef0e24482c8c2a9022953df7b5e3feed947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `openjdk:8u282-nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull openjdk@sha256:922c8e357d052ac91d08e61f94090624d646b32c89569ff13c1434f38af47c70
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.5 MB (202495338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdbcea4ebe293f9d62f13e8df835ac4e131222c73370bb6877d47f1c2fd9a18`
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
# Wed, 14 Apr 2021 17:28:01 GMT
COPY dir:6f6bc9ea1f93ff1db59b5fd63225d3a5b1df7d373dee2c520410df56c408f0e1 in C:\openjdk-8 
# Wed, 14 Apr 2021 17:28:22 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version 	&& echo Complete.
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
	-	`sha256:f188468a9a363e71d7326b17214fd697ff6df37bd2fc55e006cdc660323e0e75`  
		Last Modified: Wed, 14 Apr 2021 17:54:39 GMT  
		Size: 101.0 MB (100991372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74ed7bebf35056ba98bc3850f4881532a43518de6667c048babd96c6e2cb0e5`  
		Last Modified: Wed, 14 Apr 2021 17:54:26 GMT  
		Size: 92.0 KB (92027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
