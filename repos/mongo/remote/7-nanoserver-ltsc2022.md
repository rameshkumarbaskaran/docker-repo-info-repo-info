## `mongo:7-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:a9b97ab7976a5dad1e9c4f8e535282214319491add51920f8f89148237bbc23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `mongo:7-nanoserver-ltsc2022` - windows version 10.0.20348.2159; amd64

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
