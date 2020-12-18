## `golang:rc-nanoserver-1809`

```console
$ docker pull golang@sha256:c2a1c34b2e0f8081a3b49c5802f12cb9781d25166b98967710f18852590a517e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `golang:rc-nanoserver-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull golang@sha256:f9b1b1ea9506ef2e9bdc67c9c4b1006c5b226992bc7ffa134cf708ed4fe3a137
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242542961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9696c1bf2d276f6bd8729c3187d2631525dbccf491dce3a799ff5874def24a7e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 13:41:58 GMT
SHELL [cmd /S /C]
# Wed, 09 Dec 2020 13:41:58 GMT
ENV GOPATH=C:\gopath
# Wed, 09 Dec 2020 13:41:59 GMT
USER ContainerAdministrator
# Wed, 09 Dec 2020 13:42:15 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\go\bin;%PATH%"
# Wed, 09 Dec 2020 13:42:15 GMT
USER ContainerUser
# Fri, 18 Dec 2020 19:21:50 GMT
ENV GOLANG_VERSION=1.16beta1
# Fri, 18 Dec 2020 19:23:51 GMT
COPY dir:fe45976183cf47f1df4a6b9396bda159420262c0698162187c395ffdd2f3f955 in C:\go 
# Fri, 18 Dec 2020 19:24:11 GMT
RUN go version
# Fri, 18 Dec 2020 19:24:12 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ef62a6c873d742d2352d72aa47cbe24e03af8176a7a65e82afc21e7ce96268ea`  
		Last Modified: Wed, 09 Dec 2020 13:56:30 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4205eb72db05f020d79acbdc856520ee378829d913710e9515a412b6989e1b2`  
		Last Modified: Wed, 09 Dec 2020 13:56:29 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b7945a0e13b94f56a6a71a712e89439fbcd9d0c261d03dec9f6acb55654b0`  
		Last Modified: Wed, 09 Dec 2020 13:56:28 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f1bd520f12866b93e98eccb99b343aecc0e009c059872eae2dfb46899519d4`  
		Last Modified: Wed, 09 Dec 2020 13:56:29 GMT  
		Size: 64.3 KB (64336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44b7628f5b5064fb21e8bcb843efa4aa8db9073a95e47098b17b3b32ed95e0c`  
		Last Modified: Wed, 09 Dec 2020 13:56:26 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7838436377f654b627ec4fcf6cb6c94a82f7a7c25126cd674f48c73921b99c`  
		Last Modified: Fri, 18 Dec 2020 19:27:31 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017935fff3abf215db9ce26219edd798106b1c0f7ec22f83f0026d1eff4354b6`  
		Last Modified: Fri, 18 Dec 2020 19:28:08 GMT  
		Size: 141.1 MB (141143523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f51f998222637dd70d06b28a2db6f5f906da4b6bc794c597f88790ec6dcdfe`  
		Last Modified: Fri, 18 Dec 2020 19:27:31 GMT  
		Size: 64.8 KB (64792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d6ff20615af2374739b2e233a2b893c63f973dfde9a4467567e8ce03003b6f`  
		Last Modified: Fri, 18 Dec 2020 19:27:31 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
