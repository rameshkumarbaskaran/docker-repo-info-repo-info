## `openjdk:17-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:4687d7b32e2e64676bf2eda0c3d7b47699aa7b72ccddf03d4dc1b5d3d7c0ed6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `openjdk:17-ea-nanoserver-1809` - windows version 10.0.17763.1817; amd64

```console
$ docker pull openjdk@sha256:301a0729deb572c30cc976dd843dc0f1e0b24c86786e7749d4fcbe9d0eb49916
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285712990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57d43dc73536ceccc67bbf561df08c476b132ef6505852d3aa13961d1f1dc5f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 26 Feb 2021 16:47:31 GMT
RUN Apply image 1809-amd64
# Wed, 10 Mar 2021 17:50:47 GMT
SHELL [cmd /s /c]
# Wed, 10 Mar 2021 17:50:48 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Mar 2021 17:50:49 GMT
USER ContainerAdministrator
# Wed, 10 Mar 2021 17:51:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Mar 2021 17:51:08 GMT
USER ContainerUser
# Fri, 26 Mar 2021 00:51:55 GMT
ENV JAVA_VERSION=17-ea+15
# Fri, 26 Mar 2021 00:52:13 GMT
COPY dir:e21e29fa7fe77e9663e06e1a5ae2d219d32b22bca6d280184b656e9956f32f85 in C:\openjdk-17 
# Fri, 26 Mar 2021 00:52:39 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 26 Mar 2021 00:52:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a11c4ca8f1ba16b6e1395d4523be2215bd0871c2e3e4695b9f2b87bd7472be52`  
		Size: 101.4 MB (101389964 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b1146273d9b624ee892dfcbb3c753523f09f79536a16d63b711cb0027825374a`  
		Last Modified: Wed, 10 Mar 2021 18:33:51 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c1ac1e6f2d0594fe7e8e0395310c60461fc8ce5183f6a15db964a07b66176e`  
		Last Modified: Wed, 10 Mar 2021 18:33:51 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050de60c3748a5bfc798f599cadba652e52a162ca31f36b8c783664c11ed224b`  
		Last Modified: Wed, 10 Mar 2021 18:33:54 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e309359702f2d5c4fa7bc854144ad320712050892d017cdfcb58acff4fea2609`  
		Last Modified: Wed, 10 Mar 2021 18:33:50 GMT  
		Size: 66.6 KB (66576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97ecf2dccedb4699a8caf6c19a7a80768c90efb0af5959f1465b00abe8faa12`  
		Last Modified: Wed, 10 Mar 2021 18:33:48 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8807a480bcc21c0d3cefbeeda73dc4567f032e656eaeaa011598c694db79d4`  
		Last Modified: Fri, 26 Mar 2021 01:02:47 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb9381147164227f6ba5b40fedebc8e35f68a34552e5bec3f03e1af76d09dbb`  
		Last Modified: Fri, 26 Mar 2021 01:03:07 GMT  
		Size: 180.6 MB (180627121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c944adf341c72fa400dab2c0a8313e3f5c1e6d73d1449595df8f4952a28045f8`  
		Last Modified: Fri, 26 Mar 2021 01:02:48 GMT  
		Size: 3.6 MB (3622359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f173c0a241558072b8541e0ed04bef1f05cf0f86f88c517b76728cc9a9a4b6`  
		Last Modified: Fri, 26 Mar 2021 01:02:47 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
