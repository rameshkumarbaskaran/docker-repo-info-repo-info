## `mongo:4-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:7773c1b2e26b4d1495d8e5b94e77d3d574522224d0e2b94e5624d1d7fbe3309a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `mongo:4-nanoserver-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull mongo@sha256:240cdb4f3c89103a6064afd1d5877be4f5e8824cb152d304ca4522b0382cfba3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.9 MB (365851461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f022e78ef52f11a029cbd334c09372eed47ab9b56929f52730ed0df86173d2`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 03 Aug 2023 09:40:19 GMT
RUN Apply image 10.0.20348.1906
# Thu, 10 Aug 2023 00:45:25 GMT
SHELL [cmd /S /C]
# Thu, 10 Aug 2023 01:14:21 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 01:14:29 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 10 Aug 2023 01:14:30 GMT
USER ContainerUser
# Thu, 10 Aug 2023 01:36:00 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Thu, 10 Aug 2023 01:52:16 GMT
ENV MONGO_VERSION=4.4.23
# Thu, 10 Aug 2023 01:52:38 GMT
COPY dir:739eedf5b611d7ab486a081d1bba37f7b41d267250aae84c5635032df3e67f22 in C:\mongodb 
# Thu, 10 Aug 2023 01:52:49 GMT
RUN mongo --version && mongod --version
# Thu, 10 Aug 2023 01:52:50 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 10 Aug 2023 01:52:50 GMT
EXPOSE 27017
# Thu, 10 Aug 2023 01:52:51 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:ea9613880997b3ab2284a37c0c14a403553457b0c331b41c6bd6d1cc7838a222`  
		Last Modified: Tue, 08 Aug 2023 18:47:21 GMT  
		Size: 120.5 MB (120500677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a528e77cf0bef98e15c3b4194ee340960485498ac4c1bdcbab44307858ecfc4`  
		Last Modified: Thu, 10 Aug 2023 01:03:26 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0247382dbd5864284425d3942427091871bf5f10629f0608efbc6b3303d067`  
		Last Modified: Thu, 10 Aug 2023 01:59:00 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ffaf70bb154004aa4faefa8b8926380d11a591157ac5074e2438ce1696d3ac`  
		Last Modified: Thu, 10 Aug 2023 01:58:58 GMT  
		Size: 77.9 KB (77932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54933f30fc7826d81c7a7731e98cb5ea37dd377d70a605f59fda57f3a196506c`  
		Last Modified: Thu, 10 Aug 2023 01:58:58 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf8394a5e5cbefc5cd1d5daeced5aa9ad688b6c6fd97fc48af0020838945c4a`  
		Last Modified: Thu, 10 Aug 2023 02:16:18 GMT  
		Size: 263.4 KB (263411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867c5d9c84636930ccff9e510c8b11deb38be91c79d70f374e42b645d7d42dd5`  
		Last Modified: Thu, 10 Aug 2023 02:28:11 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df308ed75aec6217ca5d60d8570804c52378e2c7667e1101a9aa8595bc80283c`  
		Last Modified: Thu, 10 Aug 2023 02:28:54 GMT  
		Size: 244.9 MB (244948279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c794f62e01c589ca222a0b3aecdbb8bc21b93bac399efba8da896b3c9713bb0d`  
		Last Modified: Thu, 10 Aug 2023 02:28:09 GMT  
		Size: 53.3 KB (53297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6176720bc41991b8961724335617591a2f8158631c33f40595b15364d40a0b68`  
		Last Modified: Thu, 10 Aug 2023 02:28:10 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af22cc0b53ca898e53e6f427818822054d3d5d7773e87ca4a2b286584174f55`  
		Last Modified: Thu, 10 Aug 2023 02:28:09 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb6c6bd11124ed79f2ef344e4434448cca6eed7f71aca32e711e1b373043483`  
		Last Modified: Thu, 10 Aug 2023 02:28:09 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
