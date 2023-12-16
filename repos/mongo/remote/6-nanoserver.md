## `mongo:6-nanoserver`

```console
$ docker pull mongo@sha256:3ba09142ef052f9b803ad7ec92cc6a497f66c649c5b3a3f23d7b24c24216e2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2159; amd64
	-	windows version 10.0.17763.5206; amd64

### `mongo:6-nanoserver` - windows version 10.0.20348.2159; amd64

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

### `mongo:6-nanoserver` - windows version 10.0.17763.5206; amd64

```console
$ docker pull mongo@sha256:5c6c946fa3edb2aefb0bd317eac6f882d1cf7beda349007e5312da7108ac9556
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.3 MB (622342743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b52b3e3cd248f1662fffe09f48e5d5d87702399e08449686a4802a1ab4aeea`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 04 Dec 2023 10:54:04 GMT
RUN Apply image 10.0.17763.5206
# Sat, 16 Dec 2023 00:02:37 GMT
SHELL [cmd /S /C]
# Sat, 16 Dec 2023 00:02:38 GMT
USER ContainerAdministrator
# Sat, 16 Dec 2023 00:02:41 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 16 Dec 2023 00:02:42 GMT
USER ContainerUser
# Sat, 16 Dec 2023 00:02:43 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Sat, 16 Dec 2023 00:02:43 GMT
ENV MONGO_VERSION=6.0.12
# Sat, 16 Dec 2023 00:03:21 GMT
COPY dir:329dc1f21a61007915141205ec19b27dc3ea273dd304d374db84e0d8d0974daa in C:\mongodb 
# Sat, 16 Dec 2023 00:03:28 GMT
RUN mongod --version
# Sat, 16 Dec 2023 00:03:29 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 16 Dec 2023 00:03:30 GMT
EXPOSE 27017
# Sat, 16 Dec 2023 00:03:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:424f13a93a185a5defe848e7d270655e05233555f51328c0af24b9e70677d037`  
		Last Modified: Tue, 12 Dec 2023 20:02:40 GMT  
		Size: 104.5 MB (104510104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d7a1bd10386034d9ff1ea42dc85b49f215e61fc6e0fd68cc95a8f35e414ce9`  
		Last Modified: Sat, 16 Dec 2023 00:03:35 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940c7cc2a64cc8c194247c2cc2019a3beedf79785817f09447c29878b12c8762`  
		Last Modified: Sat, 16 Dec 2023 00:03:35 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cce2eec8cae129302ce3483e316a49f92c164e99f3c531f15e59159cca144c`  
		Last Modified: Sat, 16 Dec 2023 00:03:35 GMT  
		Size: 72.4 KB (72376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319a4854faf67150f88469a6cf3c0fd7f59d2fa2eab5e0e89c1878005fe37a5d`  
		Last Modified: Sat, 16 Dec 2023 00:03:35 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f59d6838522134a5b14d2bb80918a238c8901d06a2491c3d8907e885ed1ff23`  
		Last Modified: Sat, 16 Dec 2023 00:03:34 GMT  
		Size: 267.1 KB (267138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d0b10cb8fbc38b91cdbbbc26dff1b13a7f9fa746f4a51ba640b7da5badf19a`  
		Last Modified: Sat, 16 Dec 2023 00:03:34 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7be5a86c5a7ab511f33de9311bf5d8d124a48d6e0969fe14fb1a67676654d`  
		Last Modified: Sat, 16 Dec 2023 00:04:16 GMT  
		Size: 517.4 MB (517399692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8584db63e7d0c565c9af9e78dfd573ed0a0f979b267ebc6aa06326c4097cad2a`  
		Last Modified: Sat, 16 Dec 2023 00:03:33 GMT  
		Size: 85.7 KB (85701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f69d882e0d93abcba3a56445f20f8d60297302932aa9ff4f8eeacb721673c6`  
		Last Modified: Sat, 16 Dec 2023 00:03:33 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042983c924468fa0137d7c0fbaee8fae20f73a622d645882fdd6948dd65359a6`  
		Last Modified: Sat, 16 Dec 2023 00:03:33 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697febdd97236a3f64c8b78e890ef32233b815abcdc174c570bd84fab26d638b`  
		Last Modified: Sat, 16 Dec 2023 00:03:33 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
