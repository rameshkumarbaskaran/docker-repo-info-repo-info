## `eclipse-temurin:11-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:3833a9bfe84c1c9a02c72acc0ac540ecf5eb64a86121689f8c76de4632845b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `eclipse-temurin:11-nanoserver-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull eclipse-temurin@sha256:960e533396a93be38a0e6ad1f1bc9c03d997f5142040c77eb3d5c9ea2340ef10
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294691799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bfc0749d29889090797e74c00e19c7423f22ea237f4e07decebb23df344d7f1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Oct 2021 08:01:14 GMT
RUN Apply image 1809-amd64
# Wed, 13 Oct 2021 18:17:55 GMT
SHELL [cmd /s /c]
# Wed, 13 Oct 2021 18:33:29 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Wed, 13 Oct 2021 18:33:30 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 13 Oct 2021 18:33:31 GMT
USER ContainerAdministrator
# Wed, 13 Oct 2021 18:33:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Oct 2021 18:33:45 GMT
USER ContainerUser
# Wed, 13 Oct 2021 18:34:03 GMT
COPY dir:4c789b050c2a81313b7828df90f0ac6231d2beb7f7e21c1b81eca114d601d1fd in C:\openjdk-11 
# Wed, 13 Oct 2021 18:34:32 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Oct 2021 18:34:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:934e212983f208dc2bebc5de38259a6a62f1761868aacfee2cb3585a13b1e24b`  
		Size: 102.7 MB (102661372 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ceff24c3c0c2c360cd3788fcde5c41e1d6601339f4944623c732558a6030e631`  
		Last Modified: Wed, 13 Oct 2021 19:12:58 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de63d1537f04b56e93b0b7487dbb45775e91fc6634697cf3fdda8a82ed83f651`  
		Last Modified: Wed, 13 Oct 2021 19:22:31 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9359d885179b20c5f8871cc2c856c7b5d609b5c3b024b53c3e4bc7f237ae838e`  
		Last Modified: Wed, 13 Oct 2021 19:22:31 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7397577754d9a766800b16d38d25df303d1d40880a656a87d8f1ec5de0075279`  
		Last Modified: Wed, 13 Oct 2021 19:22:30 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814b69b71c6d3e48a4e089a84fa44459dd64a2734f0ec64623708ac87e844cf0`  
		Last Modified: Wed, 13 Oct 2021 19:22:28 GMT  
		Size: 71.2 KB (71249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155046e430dd658eb2e17c42b4dda04125a578e099f10d260da1811806b76549`  
		Last Modified: Wed, 13 Oct 2021 19:22:29 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3569cce016c368960469c6f69f46d259d2a70e476bacfc7a55d5e022ae3db578`  
		Last Modified: Wed, 13 Oct 2021 19:25:51 GMT  
		Size: 191.9 MB (191861247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9164340d09e91fc4325ebcdbafb35271492041355e56582057067fb0227990c`  
		Last Modified: Wed, 13 Oct 2021 19:22:29 GMT  
		Size: 91.7 KB (91691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f68e059c073e416afeb197ac4d0de3610b0cb9ad6e29c6cccd87f05bcae33e`  
		Last Modified: Wed, 13 Oct 2021 19:22:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
