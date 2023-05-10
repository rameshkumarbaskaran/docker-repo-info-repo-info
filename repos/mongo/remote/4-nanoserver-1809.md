## `mongo:4-nanoserver-1809`

```console
$ docker pull mongo@sha256:787a2e2461077b321616ff1810360c38a33f12dac0d55e7081172a696486bd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `mongo:4-nanoserver-1809` - windows version 10.0.17763.4377; amd64

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
