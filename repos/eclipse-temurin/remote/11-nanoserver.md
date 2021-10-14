## `eclipse-temurin:11-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:9792fcf63759ec6f40eaef0d9a909672cbfb233de9b6528166100ac434db2327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.288; amd64
	-	windows version 10.0.17763.2237; amd64

### `eclipse-temurin:11-nanoserver` - windows version 10.0.20348.288; amd64

```console
$ docker pull eclipse-temurin@sha256:0c2d55711d2d4d38121b74a4fbfff0cefa88c4a02228b38722018d9de5fb649b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.9 MB (308940837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011024b5ffaaf9d9f25ae1d4bba35df84035bec312e180b8d28e664db0624dc2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Oct 2021 11:15:04 GMT
RUN Apply image ltsc2022-amd64
# Wed, 13 Oct 2021 19:02:30 GMT
SHELL [cmd /s /c]
# Wed, 13 Oct 2021 19:03:51 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Wed, 13 Oct 2021 19:03:51 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 13 Oct 2021 19:03:52 GMT
USER ContainerAdministrator
# Wed, 13 Oct 2021 19:04:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Oct 2021 19:04:07 GMT
USER ContainerUser
# Wed, 13 Oct 2021 19:04:28 GMT
COPY dir:4c789b050c2a81313b7828df90f0ac6231d2beb7f7e21c1b81eca114d601d1fd in C:\openjdk-11 
# Wed, 13 Oct 2021 19:04:46 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Oct 2021 19:04:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:91284e7e8fd4bd7ebcfa98544a3e4f59639f38281225c81c34b6fe22e0dba4e5`  
		Size: 116.9 MB (116939483 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ba797e8f93823c3d71c52fcae413f3a33ca28ff2711c09ba5141432948f8298`  
		Last Modified: Wed, 13 Oct 2021 19:43:54 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb99973d4bc63fc57fe80728eb9284d6c30c79247c995760d90694a2e2c475ec`  
		Last Modified: Wed, 13 Oct 2021 19:45:10 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f4e3ec7a41b6157ede35d40a643ae557e91ef37b5271db4c11a05d21cff390`  
		Last Modified: Wed, 13 Oct 2021 19:45:10 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a57907d6771ce405ca54b1de43cce670178bbe268fe4b6afb93e3c4b9872df`  
		Last Modified: Wed, 13 Oct 2021 19:45:10 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d25c4bee418e5626e46146febfe6b1e78bab8cdf6bbf29147c380a1aa963da`  
		Last Modified: Wed, 13 Oct 2021 19:45:08 GMT  
		Size: 85.4 KB (85362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379d093b1025356b9815670b65ceb49f3d0e72fe900d7964c86f9b83f7a4d478`  
		Last Modified: Wed, 13 Oct 2021 19:45:07 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6801bfc2f012691ac354992fd5ebf68d3fb6977ee266aa972768d8921f70b7e7`  
		Last Modified: Wed, 13 Oct 2021 19:45:27 GMT  
		Size: 191.8 MB (191848320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadad310ffbdc6cd9c014be0f859162d31094999dd9558328ce7f549d87fd7e6`  
		Last Modified: Wed, 13 Oct 2021 19:45:07 GMT  
		Size: 60.7 KB (60729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e491f7dbf1ae63a77a45f31e700ab7204727ab1e72422389f4384b463fbf2a5`  
		Last Modified: Wed, 13 Oct 2021 19:45:07 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-nanoserver` - windows version 10.0.17763.2237; amd64

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
