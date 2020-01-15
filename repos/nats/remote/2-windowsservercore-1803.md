## `nats:2-windowsservercore-1803`

```console
$ docker pull nats@sha256:d06f971a89319c413118f67b67dab4e52914ad2540fcd2844f831c2a237c35d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1246; amd64

### `nats:2-windowsservercore-1803` - windows version 10.0.17134.1246; amd64

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
