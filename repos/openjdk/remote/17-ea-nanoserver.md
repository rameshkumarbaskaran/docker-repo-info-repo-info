## `openjdk:17-ea-nanoserver`

```console
$ docker pull openjdk@sha256:3ffedb6dd6f80b0b239c7559a3d5e268ab95ebf13ceb15cdbed1dc9b5014faf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `openjdk:17-ea-nanoserver` - windows version 10.0.17763.1757; amd64

```console
$ docker pull openjdk@sha256:49d9ce5246ad8262550ac08b63ee812342b77fbcdcd7853d4b156e72fd7c98c0
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286198529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063910153f04f48f930aa994754f64789aaa3adec24cf129a47410a0c4c5067d`
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
# Fri, 12 Feb 2021 23:19:08 GMT
ENV JAVA_VERSION=17-ea+9
# Fri, 12 Feb 2021 23:19:22 GMT
COPY dir:b48116cb1458fa74f0048a812652fe1edc77e6c7e04d6556ad8e3a3522ac94de in C:\openjdk-17 
# Fri, 12 Feb 2021 23:19:43 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 12 Feb 2021 23:19:44 GMT
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
	-	`sha256:61645aa8ed7c54304ec678b3cc9e5f314c79da43d8d8f6670d9961e4fcf939a0`  
		Last Modified: Fri, 12 Feb 2021 23:30:14 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f546c55a94db5fef589147f00bbaf5f249cd14f4197558e7983f62249d7f64`  
		Last Modified: Fri, 12 Feb 2021 23:30:33 GMT  
		Size: 181.0 MB (181046074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2804bb849111531bf4678749628369fbadf8b4a48d74d7baa30a6db2b6f1b706`  
		Last Modified: Fri, 12 Feb 2021 23:30:15 GMT  
		Size: 3.7 MB (3671345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f682fb6f00c43abcc09b2a5c76963bcba1ca979018c43e5c7c62e4b419daabfa`  
		Last Modified: Fri, 12 Feb 2021 23:30:14 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
