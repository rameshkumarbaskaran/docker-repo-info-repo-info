## `openjdk:jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:5f7d2f3d01b09b45172d1df7607381977e05592473fd3363143367784ebe0306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `openjdk:jdk-nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull openjdk@sha256:42c0c1e8496d507878e9ae7564c5b163db2cc705c360af6613b2903313b59557
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285112130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e91c7bf35c1da1b9d5c841e6d4984e925568e67af07c275ab57eaa2178d608`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:53:40 GMT
SHELL [cmd /s /c]
# Wed, 14 Apr 2021 17:01:24 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 14 Apr 2021 17:01:24 GMT
USER ContainerAdministrator
# Wed, 14 Apr 2021 17:01:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Apr 2021 17:01:40 GMT
USER ContainerUser
# Wed, 14 Apr 2021 17:01:40 GMT
ENV JAVA_VERSION=16
# Wed, 14 Apr 2021 17:01:59 GMT
COPY dir:03c380a356e8b0fa2d413bbd7f8427b40b2c6808fd016e7b77d87b6b5da6487b in C:\openjdk-16 
# Wed, 14 Apr 2021 17:02:21 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 14 Apr 2021 17:02:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c2c727299531adc7c2aacb1f062d72fd42cec96a0d235b3e5b0afe03e9ddbc7d`  
		Last Modified: Wed, 14 Apr 2021 17:41:13 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d8da3586de7160296948acfffc7e4146122a7dff913ba7d3a9dcdd69de8627`  
		Last Modified: Wed, 14 Apr 2021 17:43:19 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4525b9aff55d1268eee10fa04063e7bc4c375329cf1aab32caecf1915cb566a5`  
		Last Modified: Wed, 14 Apr 2021 17:43:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ba7774e6e0c9f46b40c23675b77e86192a71b8fb2295614bb08b7aa8bbbb37`  
		Last Modified: Wed, 14 Apr 2021 17:43:19 GMT  
		Size: 67.3 KB (67288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8b8ae9e0cac207d383dc46c4887e9f40af304da4dd1adcb66cb9c2ab8821ce`  
		Last Modified: Wed, 14 Apr 2021 17:43:16 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee94ca0a2fd8bd476944fcdd9c41650ea70feaf6d537e58f1ae6a83bbe3963d`  
		Last Modified: Wed, 14 Apr 2021 17:43:15 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba31058196e55e82f149d5fbc4384603453379fdb40ae1e5e590bdce97aeed6f`  
		Last Modified: Wed, 14 Apr 2021 17:43:37 GMT  
		Size: 180.0 MB (180032203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a710e17ef6ef602d46a2cb61eb484bad1b09cf3a83ccbc0b6904fc64377498f`  
		Last Modified: Wed, 14 Apr 2021 17:43:20 GMT  
		Size: 3.7 MB (3665486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3ea073c6ecb10159123abdd24079b89b3f5baa732eb133fad0bacd3422c625`  
		Last Modified: Wed, 14 Apr 2021 17:43:16 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
