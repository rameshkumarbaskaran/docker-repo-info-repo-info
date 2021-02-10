## `openjdk:17-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:8d3dd52685233cce30357d555f7f168902c8c27a940f123775fc1a46868e4bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `openjdk:17-ea-jdk-nanoserver-1809` - windows version 10.0.17763.1757; amd64

```console
$ docker pull openjdk@sha256:d746b78e41dc109a6e2419fd8791f7e6df585911a6ed0a9945b06a657d5e9ccc
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286150627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd62f61e3c4e191de57400e68fa4e60e94023590698c9121123b172b8827a93`
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
# Wed, 10 Feb 2021 16:46:04 GMT
ENV JAVA_VERSION=17-ea+8
# Wed, 10 Feb 2021 16:46:17 GMT
COPY dir:20f6b1b89449cd2d6043cf14b19a668ea48d02f09bb58513c15c1b288ce85129 in C:\openjdk-17 
# Wed, 10 Feb 2021 16:46:33 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 10 Feb 2021 16:46:34 GMT
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
	-	`sha256:887166fb7e5dbaabee7423216d15db344074a0beebcde376e6eb5692eec14a44`  
		Last Modified: Wed, 10 Feb 2021 17:17:32 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20652982127479d9b5cbd680291146964d4ff749a66f641c5d04464ad56e0d1`  
		Last Modified: Wed, 10 Feb 2021 17:20:56 GMT  
		Size: 181.0 MB (180992380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53f9dd368105ab327e17e924182e99acbe46da24623c32835d22327652a29d1`  
		Last Modified: Wed, 10 Feb 2021 17:17:33 GMT  
		Size: 3.7 MB (3677221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470c2516d3dd737363e10ab2276fd86a6203f83a434493f6e3c05b0bbcde88bf`  
		Last Modified: Wed, 10 Feb 2021 17:17:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
