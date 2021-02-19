## `openjdk:17-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:bae8270d2b06183f9edbe1a3d0fa82cd02acc5aa22ffcfe34bd3f3195323d3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `openjdk:17-ea-jdk-nanoserver-1809` - windows version 10.0.17763.1757; amd64

```console
$ docker pull openjdk@sha256:6292ffbac7423672aaf9bab4726c401a682bd0f0132a6e2f305e53099e0812ea
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286209928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61abe50620bb512fcc74a9c2ad8c52820ebe788aa55b1d35c8bd8c2244615c9f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Feb 2021 13:06:30 GMT
RUN Apply image 1809-amd64
# Wed, 10 Feb 2021 16:45:48 GMT
SHELL [cmd /s /c]
# Wed, 10 Feb 2021 16:45:49 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Feb 2021 16:45:49 GMT
USER ContainerAdministrator
# Wed, 10 Feb 2021 16:46:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Feb 2021 16:46:04 GMT
USER ContainerUser
# Thu, 18 Feb 2021 23:18:59 GMT
ENV JAVA_VERSION=17-ea+10
# Thu, 18 Feb 2021 23:19:13 GMT
COPY dir:061bd8a33669ff4dde55bdd3612ae8acbcc3e7920c3a0794aaf11893d6888c03 in C:\openjdk-17 
# Thu, 18 Feb 2021 23:19:39 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 18 Feb 2021 23:19:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ba17af31b9276ee11fdf859681b442db50979a39eff4cea2a559a5755cedbe01`  
		Size: 101.4 MB (101406193 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:89effbaeeb74323a670701c3b9dac248927e603ffb2d7efed14d993d32f7c183`  
		Last Modified: Wed, 10 Feb 2021 17:17:35 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba245c3ca8dc95a5fefadb2d7b2366434552cc96ad3951f7028404924978fe3`  
		Last Modified: Wed, 10 Feb 2021 17:17:35 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1331b1edc6cf93ddcbfd0ea0179ca55d1bc1fd44fee36a6d4260248d6207a6`  
		Last Modified: Wed, 10 Feb 2021 17:17:35 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ea90039b4b8e858352f401598e9a3aab5416bb5c88d71cc86d8cd325fe8586`  
		Last Modified: Wed, 10 Feb 2021 17:17:34 GMT  
		Size: 68.2 KB (68240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612927d1022d536248e669e8c4abbee53b84db28247493cf7238816707bc0e1e`  
		Last Modified: Wed, 10 Feb 2021 17:17:32 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b9eee95f4a806894577dc75134f436059dcd3b2d16a0659f9357b3531b8f3a`  
		Last Modified: Thu, 18 Feb 2021 23:30:24 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e136585f9a6692b5cb10a6ad909e68f4b9332ca52a0dd54ad788aed070d11c`  
		Last Modified: Thu, 18 Feb 2021 23:33:57 GMT  
		Size: 181.1 MB (181054322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f3abca4579d52afd98725fba967b0c10582ac78cde6df0cb4449735121811e`  
		Last Modified: Thu, 18 Feb 2021 23:30:26 GMT  
		Size: 3.7 MB (3674450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8d492f9b4179ad53915bc264e81efec1e67954ab4cd31d598ca324a76124bb`  
		Last Modified: Thu, 18 Feb 2021 23:30:26 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
