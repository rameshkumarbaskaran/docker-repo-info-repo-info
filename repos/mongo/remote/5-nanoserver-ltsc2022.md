## `mongo:5-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:c4d540465d8503ac3c1400a831f1d380ca986131dd04d200035c1515e09c769e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1726; amd64

### `mongo:5-nanoserver-ltsc2022` - windows version 10.0.20348.1726; amd64

```console
$ docker pull mongo@sha256:3a7adf348136ed930cfea4751680ea671b99d264e497da2340f04bc3e2e8289b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.5 MB (432468907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0494bcff8371385230426190677a0b66ef5f1edce987689787ffdc23f559198b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 May 2023 12:52:54 GMT
RUN Apply image 10.0.20348.1726
# Wed, 10 May 2023 01:28:38 GMT
SHELL [cmd /S /C]
# Wed, 10 May 2023 01:59:56 GMT
USER ContainerAdministrator
# Wed, 10 May 2023 02:00:07 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 May 2023 02:00:08 GMT
USER ContainerUser
# Wed, 10 May 2023 02:07:18 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 10 May 2023 02:07:19 GMT
ENV MONGO_VERSION=5.0.17
# Wed, 10 May 2023 02:07:47 GMT
COPY dir:2450b880b47cdaf2478ad323a9d506f80f8549bea4d09af6971f47574de3144e in C:\mongodb 
# Wed, 10 May 2023 02:07:59 GMT
RUN mongo --version && mongod --version
# Wed, 10 May 2023 02:08:00 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 May 2023 02:08:00 GMT
EXPOSE 27017
# Wed, 10 May 2023 02:08:01 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7d382efe6974b94c05000b6a95c1fd28e1b8bb3e81cc4592b2aa1cc46b90192c`  
		Last Modified: Wed, 10 May 2023 01:48:23 GMT  
		Size: 120.0 MB (120001338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d879624716c16bfc9a9e8c219f4a25a8d311021e41efa6a951e95c4bb6fc44`  
		Last Modified: Wed, 10 May 2023 01:47:58 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91148a7dea4dbf3b1028e81c00818780ec56bdbb7563cc6100dacaf0aef85da2`  
		Last Modified: Wed, 10 May 2023 02:25:01 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35d61dd28046e22574977fb6b4d943048979c432dd7d414debb3684a58405c4`  
		Last Modified: Wed, 10 May 2023 02:24:59 GMT  
		Size: 78.2 KB (78198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2e0389b82941ae5dd46a94665227d43b3fea67bff14cbf6ecc35cd654bb269`  
		Last Modified: Wed, 10 May 2023 02:24:59 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53e50933b5a40ecf4eaa2a19612ca2e58cc04e97d929f370bcc5597615755bb`  
		Last Modified: Wed, 10 May 2023 02:29:57 GMT  
		Size: 263.4 KB (263408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e997d5ec7f2db58a34dcbdc696699b18092755b0ccc58099f064d85ec7f38f40`  
		Last Modified: Wed, 10 May 2023 02:29:57 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e4e7b69be94a5c2f988b9544b21f884137b2a780f1846a00aba63b63bbff54`  
		Last Modified: Wed, 10 May 2023 02:30:45 GMT  
		Size: 312.1 MB (312057950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c95ffb085b052aa0ee8187c8ba361c664183ef1517baf9381dde966231f54e2`  
		Last Modified: Wed, 10 May 2023 02:29:55 GMT  
		Size: 60.4 KB (60359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4facd0601abedd09546b73a4cba8422b6b2c55b30c463ca1464fa440b0b833`  
		Last Modified: Wed, 10 May 2023 02:29:55 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d947675c4ed523e567ba3a4b024c78de498aece27318093a8e01e11900352d`  
		Last Modified: Wed, 10 May 2023 02:29:55 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64b0d3055bc2729820e767217c4ab762b820efb424eda68f2aa5efb89089c7b`  
		Last Modified: Wed, 10 May 2023 02:29:55 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
