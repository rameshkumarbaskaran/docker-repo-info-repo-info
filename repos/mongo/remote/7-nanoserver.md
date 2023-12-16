## `mongo:7-nanoserver`

```console
$ docker pull mongo@sha256:5285d2805f2d58c1b27adfbd13860a1536b04443390f1f96da9ad9db20e4d7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2159; amd64
	-	windows version 10.0.17763.5206; amd64

### `mongo:7-nanoserver` - windows version 10.0.20348.2159; amd64

```console
$ docker pull mongo@sha256:cb6b7c7aeae2e93fcb244a09b064f02fe372f7ea2dd355c8f362982cd88063a2
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **732.1 MB (732126064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93619098b4cacc8b9ac16e3e0de18b7beaf53dbf895cba550f3582f4f752b969`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 02 Dec 2023 12:14:23 GMT
RUN Apply image 10.0.20348.2159
# Fri, 15 Dec 2023 23:58:37 GMT
SHELL [cmd /S /C]
# Fri, 15 Dec 2023 23:58:38 GMT
USER ContainerAdministrator
# Fri, 15 Dec 2023 23:58:40 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 15 Dec 2023 23:58:40 GMT
USER ContainerUser
# Fri, 15 Dec 2023 23:58:41 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Fri, 15 Dec 2023 23:58:42 GMT
ENV MONGO_VERSION=7.0.4
# Fri, 15 Dec 2023 23:59:07 GMT
COPY dir:349758a11ab7f6555ea1770284f5a24923b069ce3e9a1d4cba5c34969849d2e4 in C:\mongodb 
# Fri, 15 Dec 2023 23:59:26 GMT
RUN mongod --version
# Fri, 15 Dec 2023 23:59:27 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 15 Dec 2023 23:59:27 GMT
EXPOSE 27017
# Fri, 15 Dec 2023 23:59:28 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:075332bb10f7fc70c56f7c073dd753e05cacbc93a38c181c5576739a29f8a7e1`  
		Last Modified: Tue, 12 Dec 2023 21:35:16 GMT  
		Size: 120.8 MB (120757041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e61d686518bae93e2d389b670d2f8acaff673dfaab43b8e49cf392006ffc8f`  
		Last Modified: Fri, 15 Dec 2023 23:59:35 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e0cfb6b2703f1fb9116ef4e9d31b688fca84e451b74953568560cdd4a7302e`  
		Last Modified: Fri, 15 Dec 2023 23:59:35 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d553942db9a0bc3b31d41d720615c7c18739b9e4be9b8d6a38ebceba0bb4a1e3`  
		Last Modified: Fri, 15 Dec 2023 23:59:33 GMT  
		Size: 75.5 KB (75508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c2106bc1907dfb01e9e5272d6f30e59bb742ddfda2adae3765cc6ea0b7d2cb`  
		Last Modified: Fri, 15 Dec 2023 23:59:33 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811f440b04408352671ce917244f7205e92e6cd244392584414de7bca2143e49`  
		Last Modified: Fri, 15 Dec 2023 23:59:34 GMT  
		Size: 267.1 KB (267108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b78a030e06e3ac60c3f095a03d8ae1052ca7368d551ef391d5d2e626eafdff`  
		Last Modified: Fri, 15 Dec 2023 23:59:33 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5244e726d3173d2461b2f794ed7d9919890d76b380333bd5a0294974021290e8`  
		Last Modified: Sat, 16 Dec 2023 00:00:20 GMT  
		Size: 610.9 MB (610927982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e10c03dd4840843747d91532989b7ff569a67faeb264d27a33dc79f2c58002`  
		Last Modified: Fri, 15 Dec 2023 23:59:31 GMT  
		Size: 91.1 KB (91127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b688c0c2503b6df3eaf5ee3d9d20f5b3244bb863fc59cf7ff61647f3464362`  
		Last Modified: Fri, 15 Dec 2023 23:59:31 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3cae1abd0871a110e9be2434b5fef64059364a1fc007ebb804dc9e839951bf`  
		Last Modified: Fri, 15 Dec 2023 23:59:31 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfbf2f5e4834c76fba2a0e53212b178325abc40a2ec839915f075fb213e1e3b`  
		Last Modified: Fri, 15 Dec 2023 23:59:31 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-nanoserver` - windows version 10.0.17763.5206; amd64

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
