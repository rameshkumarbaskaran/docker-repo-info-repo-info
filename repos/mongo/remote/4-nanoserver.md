## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:954f16e2d7212117e3f00edd6bc6c8cec4f3e0f256373ad87c8e677c80f82d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1906; amd64
	-	windows version 10.0.17763.4737; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.1906; amd64

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

### `mongo:4-nanoserver` - windows version 10.0.17763.4737; amd64

```console
$ docker pull mongo@sha256:01dbd9b91a9b79b95a4ecf3dd8f136e52a9872f491f6b6f3272fb2b2a9e6d3de
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.8 MB (349830284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243cafe154587e86dafa1dd6a365f6d5a2751de57997b7b128bd943844d97bb5`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 02 Aug 2023 08:33:47 GMT
RUN Apply image 10.0.17763.4737
# Thu, 10 Aug 2023 00:48:08 GMT
SHELL [cmd /S /C]
# Thu, 10 Aug 2023 01:15:48 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 01:15:57 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 10 Aug 2023 01:15:57 GMT
USER ContainerUser
# Thu, 10 Aug 2023 01:36:54 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Thu, 10 Aug 2023 01:53:03 GMT
ENV MONGO_VERSION=4.4.23
# Thu, 10 Aug 2023 01:53:26 GMT
COPY dir:739eedf5b611d7ab486a081d1bba37f7b41d267250aae84c5635032df3e67f22 in C:\mongodb 
# Thu, 10 Aug 2023 01:53:39 GMT
RUN mongo --version && mongod --version
# Thu, 10 Aug 2023 01:53:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 10 Aug 2023 01:53:40 GMT
EXPOSE 27017
# Thu, 10 Aug 2023 01:53:41 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:86fab75eb466cadf89d853682179b3b57eba9fe28c78041dd52bced81e18a627`  
		Last Modified: Tue, 08 Aug 2023 17:55:54 GMT  
		Size: 104.5 MB (104459386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298e0f667b1d8252956bc07b8438d68801dd9eb4ebb7ad345fde0bed30609680`  
		Last Modified: Thu, 10 Aug 2023 01:03:59 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814fa0d01fded994ad965ae5487dc312820ecd968291d0bb20ee608f702a9689`  
		Last Modified: Thu, 10 Aug 2023 02:00:40 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021e83a508dc7adbef323d416f3a04d3d4889d441750fa4ecf3ed425ee2e1f0`  
		Last Modified: Thu, 10 Aug 2023 02:00:39 GMT  
		Size: 69.2 KB (69188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956b7c3ad022ed0da478f25e9b64d0c5ac7947ac14c611b3d359ef414b7abf35`  
		Last Modified: Thu, 10 Aug 2023 02:00:38 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfbd46e959918de3285529745ec4e4457a85dbfa896248938b752ec62b32a7e`  
		Last Modified: Thu, 10 Aug 2023 02:17:23 GMT  
		Size: 263.4 KB (263381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec26d40096cc06ce014199357b0ad9268730997e9baa2e47f6498922e563a90`  
		Last Modified: Thu, 10 Aug 2023 02:29:07 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a17be4bd0b4545591c0faaa68bd5fce798030c99760214e18bc9f5a649d6d8f`  
		Last Modified: Thu, 10 Aug 2023 02:29:49 GMT  
		Size: 244.9 MB (244948968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2100654b04816c5b33cdab231140b16494d5c780710322a2eb53c2121b14982d`  
		Last Modified: Thu, 10 Aug 2023 02:29:06 GMT  
		Size: 81.7 KB (81708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98ad32612b57ad050e3b7a23f6a1fa5c2361c0ba253963ad50a694fe1cfd778`  
		Last Modified: Thu, 10 Aug 2023 02:29:05 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505adebd8f5dab6710ba15103ecf88c80ecb66b89020689513122e82be80e81c`  
		Last Modified: Thu, 10 Aug 2023 02:29:06 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d634660ca7ab6bc13d11249753c25deba422ed27ac6ef7ec0dadcb3cd2f80ba9`  
		Last Modified: Thu, 10 Aug 2023 02:29:05 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
