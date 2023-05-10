## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:3b8a283ee860a90d983109274a60772a8b0fa1b0548a705bc34df9c6aefe1da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1726; amd64
	-	windows version 10.0.17763.4377; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.1726; amd64

```console
$ docker pull mongo@sha256:bed83cd91bb5fc3b22e9e7693dc8c876edae1f4ea8d9d90da23f743787fcfaf8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.4 MB (365429025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250e14b6fbe2598395ecb92de926810739d8f9bb4feb6f23c90f906b227e8091`
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
# Wed, 10 May 2023 02:13:14 GMT
ENV MONGO_VERSION=4.4.21
# Wed, 10 May 2023 02:13:35 GMT
COPY dir:8ba32aff2ca9d923768f5236ed254b74cf5dce4d9a2947fd8bbd311a3e350b3d in C:\mongodb 
# Wed, 10 May 2023 02:13:45 GMT
RUN mongo --version && mongod --version
# Wed, 10 May 2023 02:13:46 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 May 2023 02:13:46 GMT
EXPOSE 27017
# Wed, 10 May 2023 02:13:47 GMT
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
	-	`sha256:74ff352af85d62b1fd1f251327cc375f021c060ea3489be5b7675c604a3b2b1b`  
		Last Modified: Wed, 10 May 2023 02:33:39 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3aabdd5b09e5211605dc17fef67ad79e445d182a7ea1afd8aa793931c6588ea`  
		Last Modified: Wed, 10 May 2023 02:34:15 GMT  
		Size: 245.0 MB (245026483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5af2830b9cc3f98723854eaded724ff51fe5e1cf3de6365420d4478a65b744`  
		Last Modified: Wed, 10 May 2023 02:33:37 GMT  
		Size: 51.9 KB (51942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463bf2e3286301bea821d1aecabebceef289d45e62ed3b09a0b8b674934043a1`  
		Last Modified: Wed, 10 May 2023 02:33:37 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707628b26875b17a63a38fc20d9a878cc3a07072a339f92062be5b828f55f02e`  
		Last Modified: Wed, 10 May 2023 02:33:37 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5594a891388a8ba37217fa0e8c22824506790e865521d6fe67d6d0d13f5e45`  
		Last Modified: Wed, 10 May 2023 02:33:37 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-nanoserver` - windows version 10.0.17763.4377; amd64

```console
$ docker pull mongo@sha256:feb908e7738b64b7cb32c50f8bf111296c80f58bb91fe36a16579bce15036324
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.8 MB (349822486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a278c0f36e18c599852dfe30dd691ce36e9209bebcaf57040a4b1bd5049fd0ef`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 01:31:05 GMT
SHELL [cmd /S /C]
# Wed, 10 May 2023 02:01:10 GMT
USER ContainerAdministrator
# Wed, 10 May 2023 02:01:23 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 May 2023 02:01:23 GMT
USER ContainerUser
# Wed, 10 May 2023 02:08:12 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 10 May 2023 02:13:53 GMT
ENV MONGO_VERSION=4.4.21
# Wed, 10 May 2023 02:14:12 GMT
COPY dir:8ba32aff2ca9d923768f5236ed254b74cf5dce4d9a2947fd8bbd311a3e350b3d in C:\mongodb 
# Wed, 10 May 2023 02:14:26 GMT
RUN mongo --version && mongod --version
# Wed, 10 May 2023 02:14:27 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 May 2023 02:14:27 GMT
EXPOSE 27017
# Wed, 10 May 2023 02:14:28 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ddac9d33b62fa0bb37c6743a1992a622e53b5bb070758474e92416b5f031ba`  
		Last Modified: Wed, 10 May 2023 01:48:38 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca1a117e5be28c4247978f3dfd437fff6feffb4a11ea43d4338f5d2b068ac76`  
		Last Modified: Wed, 10 May 2023 02:26:28 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba404708f5c409a4327ef9a8ea3e3601dd2db287f5d90c7794dada10f4ae9e69`  
		Last Modified: Wed, 10 May 2023 02:26:26 GMT  
		Size: 62.9 KB (62943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc7f80cef905cfe3aae8cf8ef021d8f598871b9df0222b4cc3f5b66899cac64`  
		Last Modified: Wed, 10 May 2023 02:26:26 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd95f6c90520d7fe9349ffc114d55efdfc3d2a4675433070a2dd42eb6d76948`  
		Last Modified: Wed, 10 May 2023 02:31:00 GMT  
		Size: 263.4 KB (263441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aeeb61e389a032a0a4f48fceb3fb20a05a93e55d29e62e670a6cf28fbeb396b`  
		Last Modified: Wed, 10 May 2023 02:34:28 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70cdb666bc9e24b65aea7d42c9d03b8fb42191ae6582fc70434eb7223fb41c4`  
		Last Modified: Wed, 10 May 2023 02:35:03 GMT  
		Size: 245.0 MB (245025387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f274fbb8f834cf91bff047519ca181c678538385915daed91cf947a963c11b`  
		Last Modified: Wed, 10 May 2023 02:34:27 GMT  
		Size: 79.2 KB (79160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4440b43c8dc56e84b0436cf94b4a486d5749ab28f5c569cd160eed060788e27e`  
		Last Modified: Wed, 10 May 2023 02:34:26 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6239c2e652af9a18a03cc12f2a1b3fb49324acf339cbdd185a28822a23e4df`  
		Last Modified: Wed, 10 May 2023 02:34:26 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8931970dbb56a6b07bc20aaa14ba72d508e7260208e5441b9ccb8adfa77fdc81`  
		Last Modified: Wed, 10 May 2023 02:34:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
