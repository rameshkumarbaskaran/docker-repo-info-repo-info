## `mongo:6-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:63472b72d088c5c1cc86884fee765ddfe248a37c793de6ab808771b8a42c6cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `mongo:6-nanoserver-ltsc2022` - windows version 10.0.20348.2159; amd64

```console
$ docker pull mongo@sha256:363e8bfea2928e95d9637769da14035df3e453bd171ae51829f484828f158dd1
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.6 MB (638616760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943b62d5bad21a67e9c6b7985c3049edafd39aab9d37efb6e933f5c32b757ed9`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 02 Dec 2023 12:14:23 GMT
RUN Apply image 10.0.20348.2159
# Sat, 16 Dec 2023 00:03:38 GMT
SHELL [cmd /S /C]
# Sat, 16 Dec 2023 00:03:38 GMT
USER ContainerAdministrator
# Sat, 16 Dec 2023 00:03:41 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 16 Dec 2023 00:03:41 GMT
USER ContainerUser
# Sat, 16 Dec 2023 00:03:43 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Sat, 16 Dec 2023 00:03:44 GMT
ENV MONGO_VERSION=6.0.12
# Sat, 16 Dec 2023 00:04:05 GMT
COPY dir:329dc1f21a61007915141205ec19b27dc3ea273dd304d374db84e0d8d0974daa in C:\mongodb 
# Sat, 16 Dec 2023 00:04:14 GMT
RUN mongod --version
# Sat, 16 Dec 2023 00:04:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 16 Dec 2023 00:04:17 GMT
EXPOSE 27017
# Sat, 16 Dec 2023 00:04:18 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:075332bb10f7fc70c56f7c073dd753e05cacbc93a38c181c5576739a29f8a7e1`  
		Last Modified: Tue, 12 Dec 2023 21:35:16 GMT  
		Size: 120.8 MB (120757041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ef67e806830ac770de2f31861ce94195a7626e4274fea6504b0e4d30c3c832`  
		Last Modified: Sat, 16 Dec 2023 00:04:23 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb77e9c5a087c7b2cee0931c81bc88e6b702556878987cb24288d020f56ab22`  
		Last Modified: Sat, 16 Dec 2023 00:04:23 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf706a972ad2420fe3026c61f56320b9d8858587722cf3b958c01d462315e0e`  
		Last Modified: Sat, 16 Dec 2023 00:04:22 GMT  
		Size: 79.9 KB (79911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaa900fc11462d5a20944cb22f51901532145aff04b6c288170ebeb09ff3850`  
		Last Modified: Sat, 16 Dec 2023 00:04:22 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4131fecc566dbdfd276a360006b127ac34b8addc5df38c1877ec43f80831401`  
		Last Modified: Sat, 16 Dec 2023 00:04:22 GMT  
		Size: 267.1 KB (267063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dedafae6dd2610351f9ac72de0587500dc4f3df2e25558de37e1f1b92974badb`  
		Last Modified: Sat, 16 Dec 2023 00:04:22 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ab18988834a6bb26ab7efac6e12b0bfab2985f1b65eeb626207240ab62c027`  
		Last Modified: Sat, 16 Dec 2023 00:05:02 GMT  
		Size: 517.4 MB (517399527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bfd62e1b64c0a3d308b418dc7d36fdc7c47851559cc0aeee7948eaa35bd6f1`  
		Last Modified: Sat, 16 Dec 2023 00:04:20 GMT  
		Size: 106.0 KB (105950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53c307bef86d3e1593f9af1fe3a5d4350f4f7a6af7104c3841da4a2b13a5de8`  
		Last Modified: Sat, 16 Dec 2023 00:04:20 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dcd10636dd3ad9796eac6736d80a1a13db966cdea8cd90171785eae71caa3b`  
		Last Modified: Sat, 16 Dec 2023 00:04:20 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90694e0bfc9d0b376de42e87a6e68d4372043f9289c5882b1bb54c7308eb95a2`  
		Last Modified: Sat, 16 Dec 2023 00:04:21 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
