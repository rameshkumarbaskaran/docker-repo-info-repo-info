## `mongo:nanoserver-1809`

```console
$ docker pull mongo@sha256:d50bada4ce46754274dfaa1a89ea99fe2cbff47706da26caa6442990670d6f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `mongo:nanoserver-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull mongo@sha256:2b380b272efcd18245435709127197760f9148b8c31d75389c74efdc326f6ee4
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.9 MB (715870735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6704e27433f56ac30164eae88180f4f23988e1f1a20bf393c12d6fd404c4faa1`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 04 Dec 2023 10:54:04 GMT
RUN Apply image 10.0.17763.5206
# Fri, 15 Dec 2023 23:56:43 GMT
SHELL [cmd /S /C]
# Fri, 15 Dec 2023 23:56:44 GMT
USER ContainerAdministrator
# Fri, 15 Dec 2023 23:56:46 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 15 Dec 2023 23:56:46 GMT
USER ContainerUser
# Fri, 15 Dec 2023 23:56:47 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Fri, 15 Dec 2023 23:56:48 GMT
ENV MONGO_VERSION=7.0.4
# Fri, 15 Dec 2023 23:57:36 GMT
COPY dir:349758a11ab7f6555ea1770284f5a24923b069ce3e9a1d4cba5c34969849d2e4 in C:\mongodb 
# Fri, 15 Dec 2023 23:57:42 GMT
RUN mongod --version
# Fri, 15 Dec 2023 23:57:43 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 15 Dec 2023 23:57:44 GMT
EXPOSE 27017
# Fri, 15 Dec 2023 23:57:45 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:424f13a93a185a5defe848e7d270655e05233555f51328c0af24b9e70677d037`  
		Last Modified: Tue, 12 Dec 2023 20:02:40 GMT  
		Size: 104.5 MB (104510104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01956648eab87760c7eff8a41c38ca14682f0fbf8990b9064ab76dca0e592d6e`  
		Last Modified: Fri, 15 Dec 2023 23:57:53 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd5d8975ec17791f225476e2d22d40d04cb0eb67d4a23ec506a0fc20065ad36`  
		Last Modified: Fri, 15 Dec 2023 23:57:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772f091f8b686d9c1c8c5caae36525daead82ee5bad5e1c61a3ed723213910db`  
		Last Modified: Fri, 15 Dec 2023 23:57:53 GMT  
		Size: 71.7 KB (71651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041ea04821a6fcabb5c3796ae906dcd27bf4d32d618dfe8ceafdac8b705b23d0`  
		Last Modified: Fri, 15 Dec 2023 23:57:51 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a6560b38310e9d12809faf2b0a64af64967d205d8d55f38e347d3376987d58`  
		Last Modified: Fri, 15 Dec 2023 23:57:51 GMT  
		Size: 267.1 KB (267056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a83d3fca064623a3c980561a22b097d1aff7374c70a8f270dde091d4d827325`  
		Last Modified: Fri, 15 Dec 2023 23:57:51 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656582f9047571253dbb3d224b0c55aa4bfd401897390384d831381c871f54b3`  
		Last Modified: Fri, 15 Dec 2023 23:58:38 GMT  
		Size: 610.9 MB (610928048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004ea4ffa949a7c5c5d0f42bd58ab1b031abd21708eac6fe025be198e0265472`  
		Last Modified: Fri, 15 Dec 2023 23:57:49 GMT  
		Size: 86.6 KB (86610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034489b73a16bd17131d294898f43f6a9a314126250f081cca5dfa2c0d82bfbb`  
		Last Modified: Fri, 15 Dec 2023 23:57:49 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd323531fc6bfbf1457b9821a83a4bec72cb8b16da0faeee06ace70f302b88`  
		Last Modified: Fri, 15 Dec 2023 23:57:49 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be221ec885d3b79cac4d26063f7bd4b153b30d265b59dc2a8c4be116e766161`  
		Last Modified: Fri, 15 Dec 2023 23:57:49 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
