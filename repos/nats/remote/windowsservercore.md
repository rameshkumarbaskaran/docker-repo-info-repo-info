## `nats:windowsservercore`

```console
$ docker pull nats@sha256:a42f0c67634d642f56a78fcc79c12b8d5d4da81b34b93f1ccb103ba2743f6e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64
	-	windows version 10.0.17134.1246; amd64
	-	windows version 10.0.14393.3443; amd64

### `nats:windowsservercore` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:f5ac96a023326f836cf1c02a5f5b30abd128056d648cac3a4643c8125532ec4f
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2230470888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ed94808574b78075af126587ee0e95fd33c3b8964fbec51c76c08c20bba3d6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Wed, 15 Jan 2020 14:40:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:41:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 Jan 2020 17:41:55 GMT
ENV NATS_SERVER=2.1.2
# Wed, 15 Jan 2020 17:41:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 15 Jan 2020 17:42:38 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 Jan 2020 17:43:46 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 15 Jan 2020 17:43:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 15 Jan 2020 17:43:49 GMT
EXPOSE 4222 6222 8222
# Wed, 15 Jan 2020 17:43:50 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 Jan 2020 17:43:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2397868e5c7aa285f662aaa9309fa4756277739e11d589a663a204df80595f2c`  
		Last Modified: Wed, 15 Jan 2020 17:10:53 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23c268ec0520ea9af1e83b69008728041b2a5f234937b9a6272d2a739fd92e`  
		Last Modified: Wed, 15 Jan 2020 17:51:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8bf81f9ddd524bd8d7611b92b362a8f558a338e038fb1a81f81872f58a76f7`  
		Last Modified: Wed, 15 Jan 2020 17:51:25 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3c94fff5bd229bc976399c1904de65b246152cd41d0147af159fd09877822a`  
		Last Modified: Wed, 15 Jan 2020 17:51:24 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e70dcd5f51d264f2ff2ba291ee37e474f5637d236d01c2d5cd8a4ab039dc60`  
		Last Modified: Wed, 15 Jan 2020 17:51:26 GMT  
		Size: 4.5 MB (4548759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b87189fe10fd6d476acc4c0869463fe1f0d813aa1fc2ff3d95efa65f86d7f34`  
		Last Modified: Wed, 15 Jan 2020 17:51:31 GMT  
		Size: 8.5 MB (8500806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a611e13685ceef48268051590fc9cc976fdec2ec0968e3a12fb9b7ef72b6f2`  
		Last Modified: Wed, 15 Jan 2020 17:51:22 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ebd020bd73cd69b61c2325da491f4c057f7fdeac1f37db60365aef9d9f56e6`  
		Last Modified: Wed, 15 Jan 2020 17:51:22 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2ef97f255816c764614a7a10afa9fa89f6b8fa9c107f24458eab08ad8aee6d`  
		Last Modified: Wed, 15 Jan 2020 17:51:22 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d555934698e4f3eaa1e7fef777b3692d4a519ec978ec5f191be9ea1a772ad6`  
		Last Modified: Wed, 15 Jan 2020 17:51:22 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.17134.1246; amd64

```console
$ docker pull nats@sha256:68c9dff50987d82ca20958b1a5ca7cb816509b6d6b024ecc0a5f83cfe26f5f59
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2368141200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f6b32275bca4375a3ca4b65ab024126e7ae1c30725dcd7ab47d638bc9c5dbc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 08 Jan 2020 15:30:02 GMT
RUN Install update 1803-amd64
# Wed, 15 Jan 2020 17:44:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:44:14 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 Jan 2020 17:44:15 GMT
ENV NATS_SERVER=2.1.2
# Wed, 15 Jan 2020 17:44:16 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 15 Jan 2020 17:45:13 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 Jan 2020 17:46:20 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 15 Jan 2020 17:46:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 15 Jan 2020 17:46:22 GMT
EXPOSE 4222 6222 8222
# Wed, 15 Jan 2020 17:46:24 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 Jan 2020 17:46:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:270ec3ad3fc7d52c0dd086b32f7751131c799e25cdcd4686cc33cbf2b607c34e`  
		Size: 699.2 MB (699246147 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dbec356e813f8f1863318efd5cd62c261f7de4ac49fc093c648020e26d0520fb`  
		Last Modified: Wed, 15 Jan 2020 17:52:17 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c748a716adbca27bf760bc535221171b42c3dcfd044a49e011295928c66c39`  
		Last Modified: Wed, 15 Jan 2020 17:52:17 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efb3710bacce94103ccc92d28b0a0af30a9bb7a29f1d7f45fc18a75e959ee2d`  
		Last Modified: Wed, 15 Jan 2020 17:52:16 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883bd0fc138e4a17c679bf7d23bb5f0186ccae58fbacdfda29c147e85e2d9383`  
		Last Modified: Wed, 15 Jan 2020 17:52:15 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:967451731bebacb830dc7e26892242d8d5c55f6576f5476820313ac2f35d2550`  
		Last Modified: Wed, 15 Jan 2020 17:52:17 GMT  
		Size: 4.9 MB (4880651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35062fb2b37da05d5d753b6519295e3b14da0bf8fecf57ba90fb507aaf498b7`  
		Last Modified: Wed, 15 Jan 2020 17:52:15 GMT  
		Size: 4.3 MB (4316097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcb4b1ca97cf159a8a5030f29505c9c52626907a92244c92d25df16333f84bf`  
		Last Modified: Wed, 15 Jan 2020 17:52:13 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a380672454ff5ba95dd36413220fa3f00b7998578a8f32ee0b85cfd6d6f9666`  
		Last Modified: Wed, 15 Jan 2020 17:52:13 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f545bb1274ec20783b4966e6592ba3ca21b327f02552a0480c57eae7bd6a77`  
		Last Modified: Wed, 15 Jan 2020 17:52:13 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29eea8dff9fd0ad0a6c1d9943b993b4519c8d7c48140eeb20de7f46fe018e764`  
		Last Modified: Wed, 15 Jan 2020 17:52:13 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.3443; amd64

```console
$ docker pull nats@sha256:f3b8aa519f1e9981b369d238e46b3e336b2df7654f7cf784b5601d5342a49137
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5739369423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ca53177d88b1126a979fb5530e66d83974e1838cecce90ade826949f5ea259`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jan 2020 15:20:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:47:08 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 Jan 2020 17:47:10 GMT
ENV NATS_SERVER=2.1.2
# Wed, 15 Jan 2020 17:47:11 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 15 Jan 2020 17:48:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 Jan 2020 17:50:09 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 15 Jan 2020 17:50:10 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 15 Jan 2020 17:50:12 GMT
EXPOSE 4222 6222 8222
# Wed, 15 Jan 2020 17:50:14 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 Jan 2020 17:50:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43da502775fb34b738d9f908cb549c2825c04f1451d1039ec99749be127e47ef`  
		Last Modified: Wed, 15 Jan 2020 17:12:02 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6771e606bb5340710c7ec7fa3294903a0a1f901e5c1e79211ee54fc1f074179a`  
		Last Modified: Wed, 15 Jan 2020 17:53:47 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8885516d0bc2df9c7e82fe0aeb847bc83415084fe85a9aed26a03b3b56ae7c`  
		Last Modified: Wed, 15 Jan 2020 17:53:46 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68459b3a704ec7e5908e23d0d52576c68eef20a4b3ede7bf88ec4e3b2321d170`  
		Last Modified: Wed, 15 Jan 2020 17:53:46 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196e19f93e85979cb0240edd67162a54a2e716e7b139c9c7a99882b3dc42fc2a`  
		Last Modified: Wed, 15 Jan 2020 17:53:47 GMT  
		Size: 5.4 MB (5383420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2ec8ad5670f9274bd1b0dbc71a9ac551d4b18d3f6254bf51bbd80049d7d9c2`  
		Last Modified: Wed, 15 Jan 2020 17:53:46 GMT  
		Size: 9.4 MB (9376638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4abd28582063a6691f03037049db18ea066600d7023aa3d2975eb66ea3cafd`  
		Last Modified: Wed, 15 Jan 2020 17:53:43 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe6eef99ce520e46eef3031fa6ebd7aeba735253cef9dd2b4e7e07255a9efd8`  
		Last Modified: Wed, 15 Jan 2020 17:53:43 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb11317f8d70c8d41b0ec7372f568029527c0809262db66d162a67d82e2ddc4d`  
		Last Modified: Wed, 15 Jan 2020 17:53:42 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3993164e2c009ccf7891a7fb2956b069daf095ac7a081307e8494e594e98fa`  
		Last Modified: Wed, 15 Jan 2020 17:53:43 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
