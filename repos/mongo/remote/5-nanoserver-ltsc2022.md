## `mongo:5-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:e849783d4faa75c332f403a00d0d7d80085ecd8ae4b425f6965d38fd53291c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.768; amd64

### `mongo:5-nanoserver-ltsc2022` - windows version 10.0.20348.768; amd64

```console
$ docker pull mongo@sha256:d0e917ff6e7a05c711d107fc563f837bda62f599fb56724fcb33c8700c0ee4f1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.5 MB (424479893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196daadeef259e82f1ef28892dfe3494b26a9e05cba24887b55278fb6c48cf79`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Jun 2022 04:10:14 GMT
RUN Apply image 10.0.20348.768
# Wed, 15 Jun 2022 13:13:03 GMT
SHELL [cmd /S /C]
# Wed, 15 Jun 2022 21:07:33 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 21:07:49 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 15 Jun 2022 21:07:50 GMT
USER ContainerUser
# Wed, 15 Jun 2022 21:07:51 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 15 Jun 2022 21:07:52 GMT
ENV MONGO_VERSION=5.0.9
# Wed, 15 Jun 2022 21:08:25 GMT
COPY dir:92accade5339a6525830f6d2f9c1964da22055a5f6e4a75b19634e461c7601bd in C:\mongodb 
# Wed, 15 Jun 2022 21:08:38 GMT
RUN mongo --version && mongod --version
# Wed, 15 Jun 2022 21:08:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jun 2022 21:08:40 GMT
EXPOSE 27017
# Wed, 15 Jun 2022 21:08:41 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:fca88290e1b048d74ec4e9d1548c4ec09dc3921f80285f39a186278fcaf2d86f`  
		Size: 118.0 MB (117976537 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:52ea757d4cfd57a7819ffb3a397488867081bb0341fe10346d64443842ef882a`  
		Last Modified: Wed, 15 Jun 2022 14:06:26 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d080cea65d065b27b84a0c594cb12010c9ccca5823ecafa6eac5ec57317d9df`  
		Last Modified: Wed, 15 Jun 2022 21:47:41 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd63edee03f035f3cfb58666e80cbb4d84af480adce8fe2ed2bd5b76c51006e`  
		Last Modified: Wed, 15 Jun 2022 21:47:38 GMT  
		Size: 86.8 KB (86778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7db326850d2b42499eea1a0f505ff09671b98a4b106c795df4d1ceac799ec0d`  
		Last Modified: Wed, 15 Jun 2022 21:47:38 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cea24d3d6cb168c05a90004e4d96708c2ee7e46f43a50bbdd82f1479bcded8`  
		Last Modified: Wed, 15 Jun 2022 21:47:38 GMT  
		Size: 263.5 KB (263517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0da4e44aaea3a39ee5220a155f6ff87a2e67300e446298dc243b0b1bdccfd86`  
		Last Modified: Wed, 15 Jun 2022 21:47:38 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2ad4a3c44609120023feaa689e8bd82b674f5982dc8b6193ecd453c8bc19bc`  
		Last Modified: Wed, 15 Jun 2022 21:52:59 GMT  
		Size: 306.1 MB (306086659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc84ed0c8fd3804eab46db8983f1e03c7a2cd04e82bc18e924e2ac61cc81f33`  
		Last Modified: Wed, 15 Jun 2022 21:47:36 GMT  
		Size: 58.2 KB (58229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d23471714bc0efc2a962e30eb2aedc64551aa5cae7e67b538c38341fc1f756`  
		Last Modified: Wed, 15 Jun 2022 21:47:36 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd56f706f38177bb25ba584854fdbe8f40ca0269f201cc4b685b33c8da7074e9`  
		Last Modified: Wed, 15 Jun 2022 21:47:36 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b8b20787c71b5301e516fcd474fee329ef167aabbd7c446c240fc98402dff`  
		Last Modified: Wed, 15 Jun 2022 21:47:36 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
