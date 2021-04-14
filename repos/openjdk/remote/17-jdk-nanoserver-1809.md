## `openjdk:17-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:77eb053ff142a06922c915ddc7fb47381a2ac45634c6b7f34705ff90a2073745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `openjdk:17-jdk-nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull openjdk@sha256:f6e80f77f5d19d6f043410301cd5edd1c018ad99ebdf69563d1df4f2ff9fe590
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286076815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6950268bd94e19359449c5d61601bf04242353540714e63166a5e8f3e36b3f76`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:53:40 GMT
SHELL [cmd /s /c]
# Wed, 14 Apr 2021 16:53:41 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 14 Apr 2021 16:53:42 GMT
USER ContainerAdministrator
# Wed, 14 Apr 2021 16:54:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Apr 2021 16:54:03 GMT
USER ContainerUser
# Wed, 14 Apr 2021 16:54:04 GMT
ENV JAVA_VERSION=17-ea+17
# Wed, 14 Apr 2021 16:54:22 GMT
COPY dir:9945bfade0f5f62abb3138c090a680fb415eb2c55b5c62ad68275ad248e75a0e in C:\openjdk-17 
# Wed, 14 Apr 2021 16:54:45 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 14 Apr 2021 16:54:46 GMT
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
	-	`sha256:4846a68a532c85058f47e1e9b777bab26eb5ad132cdeb3d646bc51d43346f1f8`  
		Last Modified: Wed, 14 Apr 2021 17:41:12 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dede727741920ec94cb8aac2b231667fd531dbedb64b47f6dddc1577123fcd85`  
		Last Modified: Wed, 14 Apr 2021 17:41:10 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7be7a926f02c08c32de5bc4e57d18923e0441090bd084aeb1b7dafaeb4ece58`  
		Last Modified: Wed, 14 Apr 2021 17:41:09 GMT  
		Size: 65.7 KB (65686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f5a6de061f5f5be316a0cf2d8471cf2baf8b3927a20b9d29826dc97bef2e54`  
		Last Modified: Wed, 14 Apr 2021 17:41:06 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ec4b9b6e6691328f2051cd1ec88ea578d4878ec3b4c3278474390697d6d2d1`  
		Last Modified: Wed, 14 Apr 2021 17:41:08 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0108eaed80c05d6cd42132fee25b3f8d04d1ccdb301f900c4edd6aa0e313d77a`  
		Last Modified: Wed, 14 Apr 2021 17:41:29 GMT  
		Size: 181.0 MB (181029751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32a6f90bbf6ce877e8bd6d9193d3ff5317654a495b2354331f21c58246ff552`  
		Last Modified: Wed, 14 Apr 2021 17:41:10 GMT  
		Size: 3.6 MB (3634256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf707e268763a32773a563b1a94f2db8f1beaffff892e06f3934c82c7dcfed9`  
		Last Modified: Wed, 14 Apr 2021 17:41:06 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
