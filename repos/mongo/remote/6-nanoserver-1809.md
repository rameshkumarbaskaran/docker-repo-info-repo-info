## `mongo:6-nanoserver-1809`

```console
$ docker pull mongo@sha256:6c348b0e4adb93e32b28c6355f706bdbb8e561495a78d03f49054f848865bfd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `mongo:6-nanoserver-1809` - windows version 10.0.17763.5206; amd64

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
