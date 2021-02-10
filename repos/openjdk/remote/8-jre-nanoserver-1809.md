## `openjdk:8-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:9b7a750a11e8f0b6df0bd6f0d16d9b3fba447e85e3e405a5f7d32829c78e4f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `openjdk:8-jre-nanoserver-1809` - windows version 10.0.17763.1757; amd64

```console
$ docker pull openjdk@sha256:44daee37f19f6359716ab654898b6a47ed3e7ff63a5ba9694e442fc79bcc4f3a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139754276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd37d8eb0c82d7b5ac5de8eec87043011f54dbdb4d99d5a4715419d494bef82b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Feb 2021 13:06:30 GMT
RUN Apply image 1809-amd64
# Wed, 10 Feb 2021 16:45:48 GMT
SHELL [cmd /s /c]
# Wed, 10 Feb 2021 17:09:45 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Feb 2021 17:09:45 GMT
USER ContainerAdministrator
# Wed, 10 Feb 2021 17:09:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Feb 2021 17:09:55 GMT
USER ContainerUser
# Wed, 10 Feb 2021 17:09:56 GMT
ENV JAVA_VERSION=8u282
# Wed, 10 Feb 2021 17:12:36 GMT
COPY dir:f51b6315789fea62bc81073100310d85cf4082234fc7f3bd9b51f6f4a883a8f3 in C:\openjdk-8 
# Wed, 10 Feb 2021 17:12:49 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:ba17af31b9276ee11fdf859681b442db50979a39eff4cea2a559a5755cedbe01`  
		Size: 101.4 MB (101406193 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:89effbaeeb74323a670701c3b9dac248927e603ffb2d7efed14d993d32f7c183`  
		Last Modified: Wed, 10 Feb 2021 17:17:35 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a706d41bb0ee41233cab7146f3efc2f3359e9297bbe0e73c22f9340e78f81bb8`  
		Last Modified: Wed, 10 Feb 2021 17:43:37 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fad09dd757e6a291e086566d4288a92ae3dad6f440adbc8291c77015854cad`  
		Last Modified: Wed, 10 Feb 2021 17:43:36 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8210e5e115ca68e1ac0bcfcd44495a42239a348a91be08db2f2bacc201c3d4e`  
		Last Modified: Wed, 10 Feb 2021 17:43:33 GMT  
		Size: 63.7 KB (63665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5331630666eeaae3550cb287d534514384d4a483ad6c68a4becbcf650c7bbf7f`  
		Last Modified: Wed, 10 Feb 2021 17:43:34 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb09ad56a0dc2efa265a9eef2f2f87bbb001eb812689041f933b9243a9684b68`  
		Last Modified: Wed, 10 Feb 2021 17:43:34 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9dddad69758512893d655a616bbbeaa2582cc4e1eb9a44d70dd2730fd99a733`  
		Last Modified: Wed, 10 Feb 2021 17:47:59 GMT  
		Size: 38.2 MB (38198632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59716be627ad0f02d1047fd6c2e28b996b0e965484df751d260c8ea010bf0eb`  
		Last Modified: Wed, 10 Feb 2021 17:47:14 GMT  
		Size: 80.6 KB (80571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
