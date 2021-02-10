## `openjdk:8-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:66eec6699901a922a487340624579ec811be68ba46ea4aa489de9466babfd5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `openjdk:8-jdk-nanoserver-1809` - windows version 10.0.17763.1757; amd64

```console
$ docker pull openjdk@sha256:ceba0564589dc0da55aa0ee0bb1ca034caac8cd6e91ce9c2fd26eb13ea2f24d7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202565168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20da300e90f4992cb1199a82ea2517a511f157231bab3a2967eb0e64db9ea416`
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
# Wed, 10 Feb 2021 17:10:07 GMT
COPY dir:6f6bc9ea1f93ff1db59b5fd63225d3a5b1df7d373dee2c520410df56c408f0e1 in C:\openjdk-8 
# Wed, 10 Feb 2021 17:10:21 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version 	&& echo Complete.
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
	-	`sha256:bc2aeac1e11c06e3ab9a6f51611989195b9018e98f46fe61a8310bf522608f7b`  
		Last Modified: Wed, 10 Feb 2021 17:45:31 GMT  
		Size: 101.0 MB (100989436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d908a48c5d75fa19ff0fe6953fcf47cbfdc972bc683407899a09f15bb4ddc8`  
		Last Modified: Wed, 10 Feb 2021 17:43:34 GMT  
		Size: 100.7 KB (100659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
