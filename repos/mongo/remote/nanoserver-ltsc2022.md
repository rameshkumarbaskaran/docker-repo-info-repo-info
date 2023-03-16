## `mongo:nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:29751f58fbcbb910df02a3247d24511195350f429fd4f7c0e10482875da2ebfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1547; amd64

### `mongo:nanoserver-ltsc2022` - windows version 10.0.20348.1547; amd64

```console
$ docker pull mongo@sha256:188b58e049dd763dd0409f1a223f0e35b54007051857408ac1786d5895f51c74
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.8 MB (636823624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da0b4919c8a61a41a7611a4301108d797e996be4c6a9606829023d58d730dff`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 07 Feb 2023 11:05:29 GMT
RUN Apply image 10.0.20348.1547
# Wed, 15 Feb 2023 23:56:24 GMT
SHELL [cmd /S /C]
# Thu, 16 Feb 2023 00:46:34 GMT
USER ContainerAdministrator
# Thu, 16 Feb 2023 00:47:15 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 16 Feb 2023 00:47:15 GMT
USER ContainerUser
# Thu, 16 Feb 2023 00:47:17 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Wed, 15 Mar 2023 22:23:45 GMT
ENV MONGO_VERSION=6.0.5
# Wed, 15 Mar 2023 22:24:35 GMT
COPY dir:8cafabdc84824168ccb42f1fb38dd461d1f5833e45f22346735df9067c52e6a6 in C:\mongodb 
# Wed, 15 Mar 2023 22:24:56 GMT
RUN mongod --version
# Wed, 15 Mar 2023 22:24:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Mar 2023 22:24:58 GMT
EXPOSE 27017
# Wed, 15 Mar 2023 22:24:59 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2e8a1636f1721beefd71f8e0c7176faabfe00d7503a69e909468fd63ac3a4992`  
		Last Modified: Thu, 16 Feb 2023 00:30:27 GMT  
		Size: 122.1 MB (122119166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a1068ea860cf7cfcf2570b406077f352946c2ab4e7cc47dafeea0ad296184c`  
		Last Modified: Thu, 16 Feb 2023 00:29:48 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db214e24db987418d45852de020b518bd1f2775c39acd283d3dc32a2d43a9cd2`  
		Last Modified: Thu, 16 Feb 2023 01:39:07 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a09543181ef38cc231e4c1aeaa8c3659c87805f41b3aa4de1846f7ecafaa5d`  
		Last Modified: Thu, 16 Feb 2023 01:39:05 GMT  
		Size: 83.3 KB (83288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778f9c80c9fc406ad9bd5c358bead14d62b3e09a69819cfd63b1fca3591c648f`  
		Last Modified: Thu, 16 Feb 2023 01:39:05 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c5820762c82f2d8598cdfeec5c188618393712d380c457660230a1e49c1cda`  
		Last Modified: Thu, 16 Feb 2023 01:39:05 GMT  
		Size: 267.1 KB (267067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61332775dd8d25d8f1df0e79d20e0e56a688f8fa65c5c8780d332027a183632f`  
		Last Modified: Wed, 15 Mar 2023 22:32:49 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47410ba49117e2592badb314dc65fad206f4028af544a2acdd2b0dee7942fd05`  
		Last Modified: Wed, 15 Mar 2023 22:34:17 GMT  
		Size: 514.3 MB (514297452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75af6ec0d59034f9c4871901cf54ac6a6277183940197a8e9f2d96a80ae7383`  
		Last Modified: Wed, 15 Mar 2023 22:32:47 GMT  
		Size: 48.7 KB (48735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ea815de7f1615a0c1d6ae4414a376546ac92b220c2ef57d4b3d0971dd8d080`  
		Last Modified: Wed, 15 Mar 2023 22:32:47 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4e61e382f5d87b032977a0e1dc0bbb55a1944d9e8d61abdd5696108277bc51`  
		Last Modified: Wed, 15 Mar 2023 22:32:47 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08177dd586bf601ac1f79eb819f5f9678792ca55d1c00b070be6daf900f5036`  
		Last Modified: Wed, 15 Mar 2023 22:32:47 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
