## `openjdk:8-nanoserver-1809`

```console
$ docker pull openjdk@sha256:b5e33772b08dfd209d0fe9e82479511024892c499a0629dedf459416aab7113a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `openjdk:8-nanoserver-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:4ec67874fb536a695b6043ccacc24d2ccd32fb242a9692ea1fdc1c52f4e55683
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201164873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e54c3dd5e334029a0f9ef675319a84e3f791692ad1ba30fff1537daf6c51e8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Jul 2020 13:50:07 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jul 2020 01:54:43 GMT
SHELL [cmd /s /c]
# Wed, 15 Jul 2020 02:34:08 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Jul 2020 02:34:09 GMT
USER ContainerAdministrator
# Wed, 15 Jul 2020 02:34:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 15 Jul 2020 02:34:25 GMT
USER ContainerUser
# Fri, 17 Jul 2020 00:02:22 GMT
ENV JAVA_VERSION=8u262
# Fri, 17 Jul 2020 00:02:55 GMT
COPY dir:bba4d92d93095aa974aa8ae4e9c21aa857106fb3a7cda2c1ce2b7787f65f8201 in C:\openjdk-8 
# Fri, 17 Jul 2020 00:03:11 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version
```

-	Layers:
	-	`sha256:dc95608099543221ef539391bfece5c1ce37b97af9da457f5990349cab028a12`  
		Size: 100.9 MB (100895619 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f6486e4debac36806ed3527d9b1baea75c1a807e26baccdd0a2f521c814273f`  
		Last Modified: Wed, 15 Jul 2020 02:43:55 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635f616413e2ffeb2b698529474f16b802473016d0380fd29b21f12527e7006d`  
		Last Modified: Wed, 15 Jul 2020 02:54:29 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a9bf2169040f2fa44109296c3dc79cd3e81ec224a0a19ae4d74f3866e4bac3`  
		Last Modified: Wed, 15 Jul 2020 02:54:29 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1401126acf0a8e1002c19605d846794b2a2e714f7bc1293cddc58869c1dc38c2`  
		Last Modified: Wed, 15 Jul 2020 02:54:27 GMT  
		Size: 63.8 KB (63805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f29752410c44cda8c2ee96c26c8abfed12f174fd499396fae2c94332705efa3`  
		Last Modified: Wed, 15 Jul 2020 02:54:27 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436fdde09e7b213f0e8a06317010e9a34201f40cd9880c49542f3cabce9401f0`  
		Last Modified: Fri, 17 Jul 2020 00:25:18 GMT  
		Size: 840.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577d924f652586edca7b45959b630bee1977d2e171725c379278b3abab8f1282`  
		Last Modified: Fri, 17 Jul 2020 00:25:30 GMT  
		Size: 100.1 MB (100110240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e7ef82c2df85fd3bc1bfa30e99b707b260d5240a7c73e82b9f773c73e10b1e`  
		Last Modified: Fri, 17 Jul 2020 00:25:19 GMT  
		Size: 90.8 KB (90813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
